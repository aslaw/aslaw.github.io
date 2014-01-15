aslaw.github.io
===============

aslaw website


This website is automatically transformed by Jekyll into a static site whenever I push this repository to GitHub.

# rbenv dependencies
git clone https://github.com/sstephenson/rbenv.git ~/.rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(rbenv init -)"' >> ~/.bashrc

# install ruby-build
git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build

# install ruby
rbenv install 1.9.3-p194

# install gemset
git clone git://github.com/jamis/rbenv-gemset.git ~/.rbenv/plugins/rbenv-gemset

# setting the ruby version and gemset (run inthe aslaw directory):
rbenv local 1.9.3-p194
rbenv gemset create 1.9.3-p194 aslaw
echo 'aslaw' >> ./.rbenv-gemsets

# install jekyll
gem install jekyll
rbenv rehash 

# create file layout (if doesnt already exist)
mkdir _layouts _posts _site
touch _config.yml
touch _layouts/default.html _layouts/

# run jekyll
jekyll serve -w


# License

The text and images on this site are Copyright 2013 by Albietz Law Firm. 
You may not reuse anything therein without my permission:
