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
- **[dns](./atividade-asa-01/dns/)** 
- **[web](./atividade-asa-01/web/)**  

✅ **[Estrutura](#Estrutura) dos serviços implementados (dns,proxy e web).**  

✅ **[Apresentação](#Apresentação) do projeto e vídeo demonstrativo.**  

✅ **[Instruções](#Instruções) para execução local.** 

✅ **[Contribuidores](#Contribuidores) do projeto.**

----
<a name="Arquitetura"></a>
## 🛠️Arquitetura 

**A arquitetura utiliza quatro containers Docker: 2 servidor web e 1 serviço de DNS e 1 Servidor proxy. O DNS resolve domínios em IPs, o servidor web processa requisições HTTP e retorna respostas, e o cliente consulta o DNS para acessar o site hospedado no servidor web por meio da URL www.asa.br . Todos se comunicam por uma rede bridge interna, garantindo isolamento e segurança.**
### 📜Diagrama da Arquitetura
![Image](https://github.com/user-attachments/assets/2e29c5b4-7a29-4ef5-859c-5fce92502147)

### Componentes
**lista dos serviços/containers utilizados com uma descrição basica**.

| Serviço | Imagem Base     | Função                          |
|---------|------------------|---------------------------------|
| `web`   |  ( Nginx )      | Servidor web que executa o site www.asa.br |
| `dns`   | (ubuntu)    | Serviço DNS para resolver o ip do servidor web.   |

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

Vídeo de execução (Visível apenas para E-mails institucionais(IFRN)):
https://drive.google.com/file/d/1PWTy6GC2HDIqfHe1YFGK0AqEx0O0bAye/view?usp=sharing
