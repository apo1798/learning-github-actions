```yml
name: Echo Action

description: 'Greet someone'

author: Leo Liao

branding:
  icon: activity
  color: white

inputs:
  user:
    description: 'user name'
    required: true
  echo-text:
    description: 'text you want to echo'
    required: false
    default: 'Welcome to my github action'

runs:
  using: composite
  steps:
    - run: echo User - ${{ inputs.user }}
      shell: bash
    - run: echo ${{ inputs.echo.text }}
      shell: bash
```
