# ASA-Entrega-02 - Docker: Conceitos e Implementação
---

## 📌 Descrição do Projeto  ![Status](https://img.shields.io/badge/Status-Funcionando-green)
**Este repositório apresenta a entrega do seminário sobre Docker, realizado para a disciplina de ASA (Administração de Sistemas Abertos) com o professor [@salesfilho](https://github.com/salesfilho).
O projeto demonstra, de forma prática:**
- 🐳 **Conceitos fundamentais do Docker**

- 🔗 **Comunicação entre containers**
https://github.com/alva010203/ASA-Entrega-02/blob/master/README.md
- 🛠️ **Implementação de serviços distribuídos**

### 🧩 O que está incluido?

✅ **[Arquitetura](#Arquitetura) do projeto e diagrama.**  

✅ **4 containers Docker e seus arquivos de configuração**.  
- **[dns](dns)** 
- **[proxy](proxy)**
- **[web](web)**
- **[web02](web02)**

✅ **[Estrutura](#Estrutura) dos serviços implementados (dns,proxy e web).**  

✅ **[Apresentação](#Apresentação) do projeto e vídeo demonstrativo.**  

✅ **[Instruções](#Instruções) para execução local.** 

✅ **[Contribuidores](#Contribuidores) do projeto.**

----
<a name="Arquitetura"></a>
## 🛠️Arquitetura 

**O projeto é composto por quatro serviços Docker: um servidor DNS personalizado que resolve domínios asa.br, um proxy reverso (Nginx) que faz o balanceamento de carga, e dois servidores web (web e web02) que servem páginas HTML. O tráfego HTTP é roteado pelo proxy com base nos nomes resolvidos pelo DNS, simulando um ambiente de rede com alta disponibilidade e resolução local de nomes..**
### 📜Diagrama da Arquitetura
![Image](https://github.com/user-attachments/assets/2e29c5b4-7a29-4ef5-859c-5fce92502147)

### Componentes
**lista dos serviços/containers utilizados com uma descrição basica**.

| Serviço | Imagem Base     | Função                          |
|---------|------------------|---------------------------------|
| `dns`   | (ubuntu)    | Serviço DNS para resolver o ip dos servidores web.   |
| `proxy`   | ( Nginx)    | Servidor que recebe requisições dos clientes e repassa para os serviços pedidos.   |
| `web`   |  ( Nginx )  | Servidor web que executa o html |
| `web02`   |  ( Nginx )  | Servidor web que executa o html |        
---
## 📁 Estrutura da atividade

projeto-asa/

├── dns/                  
│   ├── Dockerfile       
│   ├── db.asa.br        
│   └── named.conf.local 


├── proxy/                
│   ├── Dockerfile      
│   ├── default.conf      
│   └── index.html        


├── web/                  
│   ├── Dockerfile        
│   └── index.html        


├── web02/               
│   ├── Dockerfile       
│   └── index.html        


└── compose.yaml        

<a name="Apresentação"></a>
## 🖥️Apresentação projeto

### Vídeo de execução (Visível apenas para E-mails institucionais(IFRN)):
[https://drive.google.com/file/d/1PWTy6GC2HDIqfHe1YFGK0AqEx0O0bAye/view?usp=sharing]
### Apresentação pdf
[Docker.pdf](https://github.com/user-attachments/files/20031055/Docker.pdf)
---

<a name="Instruções"></a>
## 🚀 Instruções para Execução Local

### Pré requisitos
-  **Instalado docker desktop ou docker engine**
-  **Instalar o github caso vá usar o git clone**
### Execução
- **git clone https://github.com/alva010203/ASA-Entrega-01.git**
- **cd ASA-Entrega-01**
- **./service.sh dns build**    #constrói a imagem do DNS
- **./service.sh dns build**    #constrói a imagem do serviço web
- **./service.sh dns start**    #inicia o container DNS
- **./service.sh web start.**   #inicia o container WEB

---
<a name="Contribuidores"></a>
## 🤝Contribuidores
 
-[@salva010203](https://github.com/alva010203) - **Álvaro Augusto Pinheiro** 

-[Jaiir0](https://github.com/Jaiir0) - **Jairo Bezerra de Araujo**

-[yanmaia](https://github.com/yanmaia) - **Yan Ferreira Maia**
