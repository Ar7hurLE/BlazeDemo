# Teste de Performance - Blazedemo (Modo GUI)

**URL do Sistema:** [https://www.blazedemo.com](https://www.blazedemo.com)

---

## 1. Objetivo

Validar a performance do sistema simulando o cenário de compra de passagem aérea, garantindo:

- **Throughput:** 250 requisições por segundo (RPS)  
- **Tempo de resposta do 90º percentil (p90):** inferior a 2 segundos  

---

## 2. Pré-requisitos

Para executar o teste com JMeter GUI, você precisará de:

1. **Sistema Operacional**: Windows, Linux ou MacOS  
2. **Java 8 ou superior** (necessário para executar o JMeter GUI)  
   - Caso não esteja instalado, baixe e instale: [Oracle JDK](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) ou [OpenJDK](https://openjdk.org/)
3. **Apache JMeter** (GUI)  
   - Baixe a versão mais recente: [Download JMeter](https://jmeter.apache.org/download_jmeter.cgi)  
   - Extraia o arquivo ZIP em uma pasta de sua preferência

## 3. **Passos para execucão:** GUI
  1. Acesse a pasta onde o JMeter foi extraído. Dentro dela, localize a subpasta `bin`.  
  2. Execute o arquivo de inicialização do JMeter conforme seu sistema operacional:

   - **Windows:** clique duas vezes em `jmeter.bat`  
   - **Linux/Mac:** abra um terminal, navegue até a pasta `bin` e execute:
     ```bash
     ./jmeter
     ```
  3. Aguarde a inicialização da aplicação. 
  5. No menu **File → Open**, selecione o arquivo `BlazeDemo.jmx` presente no projeto.  
  2. O plano de teste está configurado com os seguintes parâmetros:  
   - **Threads (Usuários Virtuais):** 500  
   - **Ramp-up:** 10 segundos  
   - **Sampler:** HTTP Request configurado para simular a compra de passagem  

    > **Dica:** É possível ajustar o número de threads, ramp-up e duração do teste para diferentes cenários de carga.
  6. Executando o Teste:

  1. Clique no botão **Run → Start** no menu superior.  
  2. Durante a execução, você pode acompanhar os resultados em tempo real através dos seguintes painéis:    
   - **Graph Results** – para visualizar gráficos de throughput e tempo de resposta  
   - **Aggregate Report** – para obter métricas consolidadas  
  3. Aguarde a execução ser concluída e observe os Listeners.
