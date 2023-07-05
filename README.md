# DEVOPS-UDEMY
lab-devops

## VAGRANT
Dentro da pasta onde esta o VagrantFile
  # Comandos
    Para subir a máquina --> vagrant up
    Para dar reload --> vagrant reload
    Para entrar no shell da máquina --> vagrant ssh

## ANSIBLE
  No shell da máquina control-node --> vagrant ssh
    entrar na pasta plabooks --> cd /vagrant/playbooks
    
  # Comandos
    nome do playbook: ex app01.yml
    Para iniciar um playbook de maneira de teste --> ansible-playbook "nome do playbook" --check
    Para iniciar um playbook --> ansible-playbook "nome do playbook"

  # Testando a Aplicação
    Dentro do control-node/vagrant testar com curl
     - curl -H "Content-Type: application/json" --data @note.json http://app01:8080/api/notes (POST)
     - curl http://app01:8080/api/notes (GET)
     - curl -X DELETE -H "Content-Type: application/json" http://app01:8080/api/notes/1 (DELETE)