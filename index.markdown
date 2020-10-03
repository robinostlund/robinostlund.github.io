---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

<table>
  <tr>
    <td>
        <img src="/assets/img/me.jpg">
    </td>
    <td>
        Hi, my name is Robin Östlund and i am a very social guy with a deep interest in IT. With high focus on automate everything that is possbile to automate. Why redo things that you can do once?
    </td>
  </tr>
  <tr>
    <td colspan="2">
        <center>
            <img src="/assets/img/badge-aws-developer-associate.png" width="150px">
            <img src="/assets/img/badge-aws-devops-engineer-professional.png" width="150px">
            <img src="/assets/img/badge-aws-solution-architect-associate.png" width="150px">
            <img src="/assets/img/badge-aws-solution-architect-professional.png" width="150px">
        </center>
    </td>
  </tr>
</table>

<h1>Github Repositories</h1>

<table>
    <tr>
        <th>Name</th>
        <th>Description</th>
        <th>🌟</th>
    </tr>
    {% assign respositories = site.github.public_repositories | where:'fork', false | sort: 'stargazers_count' | reverse %}
    {% for repository in respositories %}
    <tr>
        <td><a href="{{ repository.html_url }}">{{ repository.name }}</a></td>
        <td>{{ repository.description }}</td>
        <td>{{ repository.stargazers_count }}</td>
    </tr>
    {% endfor %}
</table>


<!-- <h1> Last Blog Post</h1>
<h2>{{ site.posts.last.title }}</h2>
{{ site.posts.last.content }} -->
