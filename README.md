jekyll-github-plugins
=====================

Jekyll plugins for fetching data from GitHub (charts, issues, people).

# You should have environment variables set for `OCTOKIT_LOGIN` and `OCTOKIT_PASWD`

You need to set environment variables for GitHub if you want to have ability to make 5000 requests per hour (without authenticated client you will have only 60 requests), to do that, edit your .bashrc profile and add there:

```bash
export OCTOKIT_LOGIN=your-name
export OCTOKIT_PASWD=your-paswd
```

# Charts

# Issues

# People

People plugins gives you ability to git more data about people from GitHub. Only what you need to do is to copy content of /people directory to main directory with your jekyll blog and in file where you want to download GitHub users data add in Meta Data users attribute with GitHub users login and more information that overrides data downloaded from GitHub (you can override and display data with name: name, projects, description, avatar\_url, profile\_url, blog, location)

```yaml
---
users:
  pinoss:
    name: Maciej Paruszewski
    github: true
    description: Ruby developer from Wroclaw, Poland.
---
```
   
   
## Todo

1. Write tests for plugins

## Contributing

1. Fork it ( https://github.com/pinoss/jekyll-github-plugins/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
