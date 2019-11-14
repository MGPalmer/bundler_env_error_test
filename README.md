# bundler_env_error_test

See this post for the full explanation: https://monogreen.home.blog/2019/11/14/solving-bundlergemfilenotfound-or-mysteriously-missing-gem/

But in short: This is a test setup for what happens when you call one "inner" Ruby script from an "outer" directory, both with a Gemfile in it. The inner one will keep the gems set up in the outer one, and therefore will be missing its gems mysteriously. Using Bundler.with_original_env fixes this.

bundler_env_error_test $ ./wrangler 

Let's get wranglin'.
 _______________________ 
| Moo moo I'm a cow yo. |
 ----------------------- 
      \   ^__^
       \  (oo)\_______
          (__)\       )\/\
              ||----w |
              ||     ||
Traceback (most recent call last):
	1: from ./cow:5:in `<main>'
./cow:5:in `require': cannot load such file -- cowsay (LoadError)

