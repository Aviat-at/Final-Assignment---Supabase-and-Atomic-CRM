# cdevops-jenkins
Final Assignment - Supabase and Atomic CRM

TLDR;

```bash
ansible-playbook up.yaml
```

You may need some pre-requisites

1. Make sure that docker is running by doing `docker ps` until it shows 

```
CONTAINER ID   IMAGE                            COMMAND                  CREATED         STATUS         PORTS                             NAMES

```

2. run `ansible-playbook --version` to see if you have ansible. If not run:

```bash
bash <(curl -Ls https://raw.githubusercontent.com/conestogac-acsit/cdevops-bootstrap/refs/heads/main/bootstrap.sh)
```

3. run `kubectl get ns default` to see if you have a cluster. The expected result is:

```
NAME      STATUS   AGE
default   Active   29m
```

If you have another result try installing a k8s cluster:

```bash
bash <(curl -Ls https://raw.githubusercontent.com//conestogac-acsit/cdevops-bootstrap/refs/heads/main/k8s.sh)
```

This assignment consists of 4 parts of getting marmelab atomic crm running on your cluster.

### Points to Cover

## Marking

|Item|Out Of|
|--|--:|
|Part 1. Create a repository with an up.yaml and down.yaml to get supabase running on your cluster|5|
|Part 2. Create a repository on one of your gitea(s) by cloning https://github.com/marmelab/atomic-crm, and adding the other as a collaborator|5|
|Part 3. Create a jenkinsfile that updates atomic crm on your cluster every time code is pushed |5|
|Part 4. Commit a visible change to your atomic crm repository and push it. Use ngrok ingress to expose atomic crm from your cluster to the internet |5|

|||
|total|20|

