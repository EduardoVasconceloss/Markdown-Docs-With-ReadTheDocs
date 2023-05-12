# **Instalação do ReadTheDocs**

**OBS: Certifique-se que o Docker está instalado no seu ambiente**

### ReadTheDocs


### **1°** Clonar o repositório do Github 
**```git clone <u>https://github.com/EduardoVasconceloss/docker-readthedocs.git</u>```**

###  **2°** Crie um diretório na partição var e mude o nome dele 
**```mkdir rtd && chown -R 1005:205 /var/local/rtd```**

### **3°** Entre no diretório que você clonou do github e rode esse comando 
**```docker run -it -v /var/local/rtd:/data -p 8001:8000 -e RTD_PRODUCTION_DOMAIN=""IP-da-máquina":8001" -d seblon/readthedocs-docker```**

###  **4°** Agora acesse o ReadTheDocs via navegador 
**```http://"IP-da-máquina":8001```**

---
## Licença
>Desenvolvido pela equipe Tiex<br>
Autores: Eduardo Vasconcelos<br>
Data de criação: 11/05/2023
>
