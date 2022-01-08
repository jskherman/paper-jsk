---
new_page_extension: md
auto_deploy: false
admin_path: static/admin
webhook_url:
sections:
  - type: directory
    path: content
    label: Pages
    create: all
    match: "*"
  - type: directory
    path: content/posts
    label: Posts
    create: all
    match: "**/*"
upload_dir: ""
public_path: https://res.cloudinary.com/jarmos/image/upload
front_matter_path: ""
use_front_matter_path: false
file_template: ":filename:"
build:
  preview_env:
    - HUGO_ENV=staging
    - HUGO_VERSION=0.80.0
  preview_output_directory: public
  preview_docker_image: forestryio/hugo:latest
  mount_path: "/srv"
  working_dir: "/srv"
  instant_preview_command: hugo server -D -E -F --renderToDisk -d public
version: 0.80.0