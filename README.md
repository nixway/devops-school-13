Test role for build and deploy [puzzle15](https://github.com/venkaDaria/puzzle15) app.

### How to start?

Command:

```bash
ansible-playbook roles.yml -e '{"docker_login":"<login>", "docker_passwd":"<password>"}'
```
where:

- `<login>` - User login on Docker Hub
- `<password>` - User password on Docker Hub
- `~/.ssh/ansible-test` - Private key created on ec2 role and saved on localhost

### Depends:

- `amazon.aws` - `7.2.0`
- `community.docker` - `3.7.0`
