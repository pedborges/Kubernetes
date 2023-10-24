<h1>☸ Kubernetes: Provisionando um load balancer com um ingress controller</h1>

## Estes Arquivos Kubernetes serão responsaveis por:
Provisionar um serviço de loadbalancer com tres replicas que será exposta a partir de um ingress controller, sendo esta, tendo a parte de monitoramento com o grafana e observabilidade com o prometheus
![Captura de tela 2023-10-19 172644](https://github.com/pedborges/Kubernetes/assets/110577886/1ecca986-784d-4528-be99-05ebaae7c097)


## ✅ Pré requisitos:
- Criar o namespace **ingress-basic** no seu cluster Kubernetes (caso não queira este nome, alterar a referência de criação do prometheus);
- Instalar o prometheus e o grafana utilizando o helm;

-Por ser um repositório fechado, se faz necessário a criação de um arquivo **secret** para fornecermos os dados do **imagePullSecrets**

![image](https://github.com/pedborges/Kubernetes/assets/110577886/d18fe043-1761-4ff7-acb2-4ff18972faa9)

para isso a meneira mais fácil de realizarmos esse procedimento seria diretamente pelo kubectl utilizando o seguinte código (lembrando que é possível criá-lo a partir de .yaml).

**caso seja um registro público não se faz necessário este procedimento, visto que, todos terão acesso a imagem.**

![image](https://github.com/pedborges/Kubernetes/assets/110577886/e2d93dba-9566-471f-b12e-a38b90a71e8b)


## ℹ️ Dúvidas:

Acesse:

Grafana:
https://grafana.com/docs/grafana/latest/

Prometheus:
[https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal?WT.mc_id=AZ-MVP-5001893](https://prometheus.io/docs/introduction/overview/)

Ingress-nginx Controller 
[https://docs.microsoft.com/en-us/azure/developer/terraform/overview?WT.mc_id=AZ-MVP-5001893](https://kubernetes.github.io/ingress-nginx/user-guide/nginx-configuration/configmap/)https://kubernetes.github.io/ingress-nginx/user-guide/nginx-configuration/configmap/

