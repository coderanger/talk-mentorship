namespace :jekyll do

  desc 'Delete generated _site files'
  task :clean do
    system "rm -fR _site"
  end

  desc 'Run the jekyll dev server'
  task :server do
    system "jekyll --server --auto"
  end

  desc 'Clean temporary files and run the server'
  task :compile => [:clean, 'compass:clean', 'compass:compile'] do
    system "jekyll"
  end

end

namespace :compass do

  desc 'Delete temporary compass files'
  task :clean do
    system "rm -fR static/css/*"
  end

  desc 'Run the compass watch script'
  task :watch do
    system "compass watch"
  end

  desc 'Compile sass scripts'
  task :compile => [:clean] do
    system "compass compile"
  end

end
