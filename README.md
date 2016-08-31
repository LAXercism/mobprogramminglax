# mobprogramminglax

### Original problem
https://github.com/exercism/exercism.io/pull/2981

### Test PR
https://github.com/exercism/exercism.io/pull/3005  
newset PR https://github.com/exercism/exercism.io/pull/3079

--

## [Syncing the forked repository to the upstream master to keep it up-to-date](https://help.github.com/articles/syncing-a-fork/)


## git rebase
https://help.github.com/articles/about-git-rebase/


---

### To run our tests

`bundle exec rake test TEST=test/acceptance/team_test.rb`

### To run it locally
`foreman s -p 4567`

---

```ruby
git checkout master
git fetch upstream
git rebase upstream/master
git checkout team-pagination 
git rebase master 
```
git push origin team-pagination --force

---

### Using Pry

`require 'pry'; binding.pry` 

---

puts page.html


---

## [Posgres Cheatsheet](http://www.postgresonline.com/downloads/special_feature/postgresql83_psql_cheatsheet.pdf)

---

For Jen:  
To run the server locally:   
$ `rackup -s puma -p 3000 -o 0.0.0.0`

Go to the browser at:
http://0.0.0.0:3000/
