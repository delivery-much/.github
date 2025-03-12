# 🚀 Major Release v{{ version }}

This is a **major release**, marking significant changes and improvements.

{% if 'breaking-change' in pr.labels %}
  ## 🧑‍💻 Breaking Changes
  - **[breaking-change]** The following features or APIs have been removed or changed:
  {% for pr in github.event.pull_requests %}
    {{ pr.title }} by {{ pr.user.login }} in [{{ pr.html_url }}]( {{ pr.html_url }} )
  {% endfor %}
{% endif %}

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

{% if 'migration-guide' in pr.labels %}
  ## 🧑‍⚖️ Migration Guide
  - **[migration-guide]** The following migration guides are available:
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
