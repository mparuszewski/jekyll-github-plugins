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

Charts plugin gives you few simple charts with statistics about your repositories. Only what you need to do is to copy content of /charts directory to main directory with your jekyll blog and in file where you want to download GitHub charts data add in Meta Data projects with project name (user-name/project-name), and all data required for charts will be downloaded. You can use charts.html file from /charts repository and charts.js to have fully working charts. You need to download and use Highcharts (<http://www.highcharts.com/>) v4.0 to have working charts.

```yaml
---
projects:
  - pinoss/jekyll-github-plugins
---
```

# Issues

Issues plugin gives you simple, but powerfull issues filter. Only what you need to do is to copy content of /issues directory to main directory with your jekyll blog and in file where you want to download GitHub issues data add in Meta Data projects with project name (user-name/project-name), and all data required for issues will be downloaded. You can use issues.html file from /issues repository and issues.js to have fully working issues filter. You need to download Twitter Typeahead (<https://twitter.github.io/typeahead.js/>) to have working input autocomplete.

```yaml
---
projects:
  - pinoss/jekyll-github-plugins
---
```

If you have labels for your issues with same prefix, ie. 'Language-C', 'Language-Ruby' and 'Language-Python' and you want to create additional filter for your issues add to your config.yml file:

```yml
issues:
  special_filters: Lanugage Prefix1 Prefix2
```

# People

People plugin gives you ability to git more data about people from GitHub. Only what you need to do is to copy content of /people directory to main directory with your jekyll blog and in file where you want to download GitHub users data add in Meta Data users attribute with GitHub users login and more information that overrides data downloaded from GitHub (you can override and display data with name: name, projects, description, avatar\_url, profile\_url, blog, location)

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
