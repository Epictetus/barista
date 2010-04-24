# Barista

Barista is very, very similar to [bistro\_car](http://github.com/jnicklas/bistro_car) (infact, credit where credit is due - it shares similar
code / is almost a fork).

The main difference being, it lets you use coffee as you would javascript. Simply put, Write coffee
and place it in `app/scripts` and Barista will automatically serve it as if it was placed in `public/javascripts`

That is, `app/scripts/demo.coffee` will work for `/javascripts/demo.js`. Even better (and more importantly
for me), it provides `Barista.compile_all!` which takes all coffee files and compiles them into `public/javascripts`.

If you're using Jammit, this means you can simple run a rake task (`rake barista:brew` before running jammit) and
your coffeescripts will be automatically provided, ready for bundling.

To add to your project, simply add:

    gem 'barista', '>= 0.1.0'
    
To your Gemfile and run bundle install.

As you place .coffee files in app/scripts, it will automatically handle them for you.

Barista require rails 3+ (but patches for Rails 2 will be accepted.)