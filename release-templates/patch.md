# 🛠️ Patch Release v{{ version }}

This is a **patch release**, which includes bug fixes and minor improvements that ensure the stability of the project. There are no new features or breaking changes in this release.

{% if 'bugfix' in pr.labels %}
  ## 🐛 Bug Fixes
  - **[bugfix]** The following bugs have been fixed:
  {% for pr in github.event.pull_requests %}
    {{ pr.title }} by {{ pr.user.login }} in [{{ pr.html_url }}]( {{ pr.html_url }} )
  {% endfor %}
{% endif %}

{% if 'improvement' in pr.labels %}
  ## 🔧 Improvements
  - **[improvement]** Some minor improvements have been made:
  {% for pr in github.event.pull_requests %}
    {{ pr.title }} by {{ pr.user.login }} in [{{ pr.html_url }}]( {{ pr.html_url }} )
  {% endfor %}
{% endif %}

{% if 'security-update' in pr.labels %}
  ## 🧑‍⚖️ Security Updates
  - **[security-update]** Security vulnerabilities have been addressed:
  {% for pr in github.event.pull_requests %}
    {{ pr.title }} by {{ pr.user.login }} in [{{ pr.html_url }}]( {{ pr.html_url }} )
  {% endfor %}
{% endif %}

{% if 'configuration' in pr.labels %}

--- 

### ⚙️ Configuration:
- **[configuration]** Defines parameters based on the environment, and feature management controls which features are active using feature toggles.
  - **.env**: 
    - DATABASE_URL=your_database_url
    - API_KEY=your_api_key

  - **Feature Toggle**: 
    - FEATURE_X_ENABLED=true
    - FEATURE_Y_ENABLED=false
{% if 'migration-guide' in pr.labels %}

---

### 📝 Full Changelog:
- For a complete list of changes, view the full changelog: For a complete list of changes, view the full changelog: [link to changelog](${{ CHANGELOG_URL }})
