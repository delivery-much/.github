# 🚀 Minor Release v{{ version }}

This is a **minor release**, introducing new features and improvements that are backward compatible.

{% if 'feature' in pr.labels %}
  ## ✨ New Features
  - **[feature]** The following new features have been added:
  {% for pr in github.event.pull_requests %}
    {{ pr.title }} by {{ pr.user.login }} in [{{ pr.html_url }}]( {{ pr.html_url }} )
  {% endfor %}
{% endif %}

{% if 'improvement' in pr.labels %}
  ## 🔧 Improvements
  - **[improvement]** The following improvements have been made:
  {% for pr in github.event.pull_requests %}
    {{ pr.title }} by {{ pr.user.login }} in [{{ pr.html_url }}]( {{ pr.html_url }} )
  {% endfor %}
{% endif %}

{% if 'bugfix' in pr.labels %}
  ## 🐛 Bug Fixes
  - **[bugfix]** The following bugs have been fixed:
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
