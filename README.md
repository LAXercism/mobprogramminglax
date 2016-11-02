# mobprogramminglax

### Original problem
https://github.com/exercism/exercism.io/pull/2981

### Test PR
+ https://github.com/exercism/exercism.io/pull/3005  
+ Super messed up commit with good progress PR https://github.com/exercism/exercism.io/pull/3079
+ Last PR for this bug https://github.com/exercism/exercism.io/pull/3096

--

#### The files
`app/routes/teams.rb`  
`team_test.rb`  
`team_stream.rb`  
`app/routes/teams.rb`

---

## git rebase
https://help.github.com/articles/about-git-rebase/

---

### To run our tests

`bundle exec rake test TEST=test/acceptance/team_test.rb`

===

### To run exercism locally
`foreman s -p 4567`

For Jen to run the server locally:   
$ `rackup -s puma -p 3000 -o 0.0.0.0`

Go to the browser at: http://0.0.0.0:3000/

===

### Create the page to view it
+ Add pry
```
    with_login(user) do
      visit("/teams/some-team/streams?per_page=2")
      require 'pry'; binding.pry
      click_link("2")
    end
```
+ Run the tests with pry
`bundle exec rake test TEST=test/acceptance/team_test.rb`

+ Run this in the pry repl:

`target = open('page.html', 'w')`

`target.write(page.html)`

`target.close`

+ BE SURE TO EXIT PRY!
$ exit

---

### To update the branch to match with upstream
```
git checkout master
git pull upstream master
git checkout branch-name
git rebase master
```

---

```
git checkout master
git branch -m team-pagination team-pagination-mess
git checkout -b team-pagination
git cherry-pick eb6c6fe..faa36ad
git push origin team-pagination --force
```

---

#### Using Pry

`require 'pry'; binding.pry` 

---

#### [Posgres Cheatsheet](http://www.postgresonline.com/downloads/special_feature/postgresql83_psql_cheatsheet.pdf)

---

#### [Syncing the forked repository to the upstream master to keep it up-to-date](https://help.github.com/articles/syncing-a-fork/)
