namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end
  
  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do  
  desc 'migrates the db'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seeds the db'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end

task :environment do
  require_relative './config/environment'
end