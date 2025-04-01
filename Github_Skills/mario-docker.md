# Mario Docker Game in Azure

This GitHub guides the usage of terraform, azure cli and ansible to create and deploy a Mario Docker Game.

## Steps

### Navigate and follow the instructions in

1. Realizar fork al repositorio `https://github.com/ChristianFlor/training-ansible`

2. Abrir Git Bash en el proyecto y correr el comando:

`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

Con esto generaremos una clave publica y una clave privada en el directorio

3. Crear el archivo `providers.tf` para definir el proveedor Azure que usaras con Terraform 

4. Crear el archivo `variables.tf` para parametizar el despliegue

5. Crear el archivo `outputs.tf` para obtener facilmente la IP publica

6. Crear el archivo `main.tf` donde se crean los recursos en Azure

7. Inicializar Terraform:

`terraform init`

8. Desplegar la infraestructura:

`terraform plan
terraform apply -auto-approve`

9. Obtener la ip publica generada:

`terraform output public_ip_address`

10. Modificar el archivo `hosts.ini` con la direccion publica generada

11. Ejecutar los playbooks con Ansible:

`ansible-playbook playbooks/install_docker.yml
ansible-playbook playbooks/run_container.yml`

## Results

![Image mario docker](https://github.com/user-attachments/assets/078afd81-768a-47cb-9100-6867beb26710)
