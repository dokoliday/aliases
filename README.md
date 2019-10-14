# aliases

alias dki='docker images'
alias dkc='docker ps -a'
alias dkuplog='docker-compose up -d && docker-compose logs -f'
alias dkstopall='sudo docker stop $(docker ps -a -q)'
alias dkrmall='sudo docker rm $(docker ps -a -q)'
alias dkrmiall='sudo docker rmi $(docker images -q)'

alias wholisten="sudo lsof -i -P -n | grep LISTEN"

alias gst="git status"
alias gco="git checkout"
alias gc="git commit"
alias ga="git add"
alias clscreen='printf "\033c"'

function dockerNode() {
SCRIPTPATH="$( cd "$(dirname "$0")" ; pwd -P )"
docker run -ti -v $SCRIPTPATH/:/app --network=host $1 /bin/bash 

}


