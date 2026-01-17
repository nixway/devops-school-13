Test role for build and deploy [puzzle15](https://github.com/venkaDaria/puzzle15) app.

### How to start?

Command:

```bash
ansible-playbook docker_login.yml -e '{"docker_login":"<login>", "docker_passwd":"<password>"}' --private-key ~/.ssh/ansible-test
```
where:

- `<login>` - User login on Docker Hub
- `<password>` - User password on Docker Hub

### Depends:

- `amazon.aws` - `11.0.0`
- `community.docker` - `5.0.5`
