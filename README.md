# SPFC Libertadores 2025 - GCP Deploy

Este projeto tem como objetivo coletar e processar dados sobre os jogadores do São Paulo FC  para a sua campanha na **Libertadores 2025**, utilizando a **API AllSports**. Todo o processamento dos dados foi realizado em uma **máquina virtual (VM)** na **Google Cloud Platform (GCP)**, com os dados sendo armazenados em um **bucket do Google Cloud Storage (GCS)**.

## Funcionalidades

- **Coleta de Dados**: O projeto faz requisições para a API AllSports para coletar informações dos jogadores do São Paulo FC.
- **Processamento e Armazenamento**: Os dados obtidos são processados e armazenados em um arquivo JSON.
- **Deployment em GCP**: O código foi implantado em uma instância Ubuntu na Google Cloud Platform, onde a VM acessa o bucket para realizar a coleta e processamento dos dados.

## Como Funciona

1. **API AllSports**: A API é utilizada para coletar os dados dos jogadores do São Paulo FC.
2. **Bucket GCP**: Os dados processados são armazenados em um bucket no Google Cloud Storage, permitindo o acesso de qualquer instância virtual da GCP.
3. **Máquina Virtual (VM)**: Uma instância Ubuntu da GCP é configurada para acessar o bucket, realizar a coleta dos dados e processá-los localmente.

## Tecnologias Usadas

- **Python**: Linguagem de programação utilizada para a coleta e processamento dos dados.
- **API AllSports**: Fonte dos dados sobre os jogadores do São Paulo FC.
- **Google Cloud Platform (GCP)**: Infraestrutura na nuvem utilizada para o deploy do projeto, incluindo o bucket e a VM.
- **Google Cloud Storage (GCS)**: Armazenamento de dados no bucket na nuvem.
- **GitHub**: Repositório de código onde o projeto está hospedado.

## Estrutura do Projeto

- `spfc_libertadores.py`: Script principal que coleta, processa e salva os dados.
- `dados_jogadores_spfc.json`: Arquivo JSON que contém os dados dos jogadores do São Paulo FC.
- `requirements.txt`: Arquivo com as dependências necessárias para rodar o projeto.

## Como Rodar Localmente

1. Clone o repositório:
    ```bash
    git clone https://github.com/Gustavo-Pasciano93/SPFC-GCP-Deploy.git
    ```
2. Instale as dependências:
    ```bash
    pip install -r requirements.txt
    ```
3. Execute o script para coletar e salvar os dados:
    ```bash
    python spfc_libertadores.py
    ```

## Deploy em Google Cloud Platform (GCP)

1. Crie um **bucket no Google Cloud Storage** para armazenar os dados.
2. Configure uma **máquina virtual (VM)** na GCP com o sistema Ubuntu e instale as dependências necessárias.
3. Acesse o bucket na VM usando o comando `gsutil` para baixar ou fazer upload de arquivos.
4. Execute o script na VM para coletar e processar os dados e salvar no bucket.

## Como Contribuir

Sinta-se à vontade para fazer melhorias no projeto ou adicionar novas funcionalidades! Para contribuir:

1. Faça um fork do repositório.
2. Crie uma branch para a sua modificação (`git checkout -b minha-modificacao`).
3. Faça as modificações e adicione testes, se necessário.
4. Faça um commit das suas alterações (`git commit -m 'Adicionando nova funcionalidade'`).
5. Faça o push para sua branch (`git push origin minha-modificacao`).
6. Abra um pull request explicando suas alterações.

## Licença

Este projeto está licenciado sob a MIT License - consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

---

Projeto desenvolvido por **Gustavo Pasciano** para fins educacionais e de experiência com GCP e integração de dados.

## Links Úteis

- [Google Cloud Platform](https://cloud.google.com/)
- [API AllSports](https://allsportsapi.com/)
- [GitHub](https://github.com/SeuUsuario)
