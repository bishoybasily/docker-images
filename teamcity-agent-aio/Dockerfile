FROM jetbrains/teamcity-agent:2019.2.4
RUN curl -L https://github.com/docker/compose/releases/download/$(curl https://api.github.com/repos/docker/compose/releases/latest | jq .name -r)/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose && chmod +x /usr/local/bin/docker-compose
RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl
RUN chmod +x ./kubectl
RUN mv ./kubectl /usr/local/bin
