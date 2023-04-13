project('preprocess', 'fortran')

fc = meson.get_compiler('fortran')

add_project_arguments('-Dfoo=HelloWorld', language: 'fortran')

pp_files = fc.preprocess(['file.f90', 'file2.f90'], output: '@PLAINNAME@')

foreach f : pp_files
  message(f.full_path())
endforeach

lib = library('libfortran', sources : pp_files)
