+++
date = "2017-08-27T23:52:21-05:00"
title = "My baby steps with Ruby"
categories = ["Programming"]
tags = []

+++

I want to share how to create a web application with Ruby. Nevertheless, before we can start to create our amazing project, We require rbenv and Sinatra gem .... So, let's start with our recipe book!

###  Installation
1.  **rbenv** Help us management of multiply Ruby environments. In our terminal, run the following commands
  * <code> brew install rbenv </code> For installing rbenv
  * <code> rbenv install -l </code> List all versions
  * <code> rbenv install 2.4.1 </code> In our example, we use the last Ruby version
  * <code> 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.zshrc </code>
  * <code> echo 'eval "$(rbenv init -)"' >> ~/.zshrc </code>

Depending upon your bash configuration, substitute <code> ~/.zshrc </code>

2. **SINATRA**  focuses on "quickly creating web-applications" in Ruby with minimal effort
  * <code> gem install sinatra </code>

### Cookbook
- Creating a ruby file called app.rb,  we copy the code from sinatra website's doc <br/>
  <code> require 'sinatra' </code><br/>
  <code>get '/frank-says' do</code><br/>
      <code>'Put this in your pipe & smoke it!' </code><br/>
  <code>end </code>
- We can run our app, just typing in the terminal <code>ruby app.rb </code>
