desc 'outputs hello to the terminal'
namespace :greeting do
task :hello do
  puts "hello from Rake!"
end
end

desc 'outputs hola to the terminal'
namespace :greeting do
task :hola do
  puts "hola de Rake!"
end
end

desc 'migrate changes to your database'
namespace :db do
task :migrate => :environment do
  Student.create_table
end
end

task :environment do
  require_relative './config/environment.rb'
end

desc 'seed the database with some dummy data'
namespace :db do
task :seed do
  require_relative './db/seeds.rb'
end
end

desc 'pull up pry in the console'
task :console => :environment do
  Pry.start
end
