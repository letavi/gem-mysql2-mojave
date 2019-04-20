# Gem mysql2 on Mojave

Problem
========================================
Installing `mysql2` gem errors on MacOS Mojave. 

Solution
========================================
Make sure `openssl` is installed on Mac via Homebrew.
```
brew install openssl
```

Install `mysql2` gem.
```
gem install mysql2 -v '0.5.2' -- --with-ldflags=-L/usr/local/opt/openssl/lib --with-cppflags=-I/usr/local/opt/openssl/include
```