# Simple-Ruby-Dynamic-Greeter-Web-Application-Using-Sinatra-Framework-
# A professional Ruby project demonstrating a simple web application
# built with the Sinatra framework. It includes a homepage, an about page,
# and dynamic routes to greet users by name. This project is designed to
# showcase Ruby’s simplicity, Sinatra’s lightweight web capabilities, and
# how to handle HTTP requests dynamically.

require 'sinatra'

# Homepage
get '/' do
  <<-HTML
  <h1>Welcome to the Ruby Dynamic Greeter Web Application 👋</h1>
  <p>This project is powered by <b>Ruby</b> and the <b>Sinatra Framework</b>.</p>
  <p>Navigate to the <a href="/about">About Page</a> to learn more.</p>
  <p>Or try a personalized greeting: <a href="/hello/YourName">Say Hello</a></p>
  HTML
end

# About page
get '/about' do
  <<-HTML
  <h1>About This Project</h1>
  <p>This is a simple Ruby-based web application created using the Sinatra framework. 🚀</p>
  <p>It demonstrates:</p>
  <ul>
    <li>Basic web routing with Sinatra</li>
    <li>Dynamic content rendering</li>
    <li>Clean and minimal Ruby code structure</li>
  </ul>
  HTML
end

# Dynamic greeting route
get '/hello/:name' do
  name = params[:name].capitalize
  <<-HTML
  <h1>Hello, #{name}! 👨‍💻</h1>
  <p>Welcome to the Ruby Dynamic Greeter Web Application.</p>
  <p>This page was generated dynamically using Ruby and Sinatra.</p>
  HTML
end

# Run with: ruby ruby_web_app.rb
# Visit: http://localhost:4567
