+++
date = "2017-08-27T23:52:21-05:00"
title = "My baby steps with Ruby"
categories = ["Programming"]
tags = ["Programming", "Ruby", "Sinatra"]

+++

I want to share how to create a easy web application with Ruby and Sinatra. Nevertheless, before we can start to create our amazing project, We require rbenv and, of course, Sinatra gem .... So, let's start with our recipe book!

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
  <div style="background: #f8f8f8;">
    <pre>
      <span style="color:#a2f; font-weight: bold;"> require</span> <span style="color: #00f">'sinatra'</span>
      <span style="color: #a2f; font-weight: bold;" >get </span> <span style="color: #000">'/frank-says'</span> <span style="color: #a2f; font-weight: bold;">do</span>
        <span style="color: #b44">'Put this in your pipe & smoke it!'</span>
       <span style="color:#a2f; font-weight: bold;">end</span>
    </pre>
  </div>

  We can run our app, just typing in the terminal <code>ruby app.rb </code>
   To visualize our message, in a browser we direct to localhost, 4567 port!

- **bundler** provides an environment of Ruby projects by installing the exact gems and versions that are needed. Just run the following command <code>bundle init</code> and we start working. It's genereted a Gemfile file which contains a list of gems for use in our application. <br/><br/>
- **Rake** is a Make-like program implemented in Ruby. <code>gem insall rake</code> And in rakefile, I want to run my app just typing <code>rake</code> in the terminal so, I defined the following task:
 <div style="background:#f8f8f8;">
    <pre>
      <span style="color: #A2F; font-weight: bold;"> task </span><span style="color: #00F">default: </span> <span style="color: #b44">%w[runapp]</span>
        <span style="color: #A2F; font-weight: bold;">task </span> <span style="color: #c00">:runapp </span><span style="color: #a2f; font-weight: bold;">do</span>
          <span style="color: #000 ">sh</span> <span style="color: #b44">"bundle exec ruby app.rb"</span>
        <span style="color: #a2f; font-weight: bold;"> end </span>
    </pre>
 </div>
- Now! We are going to create our view in ruby with erb extension within views directory
- **Routes** In Sinatra, a route is an HTTP method, each route is associated with a block. In app.rb file, I want that in the root '/' it is shown my index view.

 <div style="background:#f8f8f8;">
  <pre>
  <span style="color: #a2f; font-weight: bold;">get </span><span style="color: #00f; font-weight: bold;"> '/' </span><span style="color: #a2f; font-weight: bold;">do </span>
     <span style="color: #a2f; font-weight: bold;">erb </span> <span style="color: #c00;">:index </span>
  <span style="color: #a2f; font-weight: bold;">end</span>
 </pre>
</div>
- **MySQL** Installing mysql gem to connect our app to data base <code style""> gem install mysql2</code>
