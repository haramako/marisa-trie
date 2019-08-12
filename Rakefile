task :linux do
  build_dir = 'build/linux'
  bin_dir = 'bin/linux'
  Dir.chdir build_dir do
    sh 'cmake', '../..'
    sh 'cmake', '--build', '.'
  end
  mkdir_p bin_dir
  cp FileList["#{build_dir}/tools/marisa-*", "#{build_dir}/**/*.a"], bin_dir
end

task :win64 do
  build_dir = 'build/win64'
  bin_dir = 'bin/win64'
  sh 'cmake', '-S', '.', '-B', build_dir, '-G', 'Visual Studio 15 2017 Win64'
  sh 'cmake', '--build', build_dir
  mkdir_p bin_dir
  cp FileList["#{build_dir}/tools/**/*.exe", "#{build_dir}/**/*.lib"], bin_dir
end

task :clean do
  rm_rf 'build'
end
