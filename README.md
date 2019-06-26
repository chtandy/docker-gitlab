docker exec -it gitlab update-permissions



/opt/gitlab/embedded/bin/runsvdir-start: line 24: ulimit: pending signals: cannot modify limit: Operation not permitted
```
sudo chmod 2770 ./srv/gitlab/data/git-data/repositories
```

```
For a comprehensive list of configuration options please see the Omnibus GitLab readme
https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/README.md
 
If this container fails to start due to permission problems try to fix it by executing:
 
  docker exec -it gitlab update-permissions
  docker restart gitlab
```

```
sudo setfacl -mR default:group:docker:rwx /srv/gitlab
```

[官方gitlab](https://docs.gitlab.com/omnibus/docker/)
