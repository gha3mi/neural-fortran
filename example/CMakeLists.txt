foreach(execid
  cnn_mnist
  cnn_from_keras
  dense_mnist
  dense_from_keras
  get_set_network_params
  network_parameters
  simple
  sine
  quadratic
)
  add_executable(${execid} ${execid}.f90)
  target_link_libraries(${execid} PRIVATE
    neural-fortran
    h5fortran::h5fortran
    jsonfortran::jsonfortran
    ${LIBS}
  )
endforeach()
