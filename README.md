<h1 align="center">
  <br>
  📞 ActionCall - Sistema de Telemarketing Inteligente
  <br>
</h1>

<h4 align="center">Plataforma premium de distribuição de leads e gestão de operações de telemarketing ativo.</h4>

<p align="center">
  <a href="#sobre-o-projeto">Sobre</a> •
  <a href="#funcionalidades">Funcionalidades</a> •
  <a href="#tecnologias">Tecnologias</a> •
  <a href="#acesso-ao-projeto">Demonstração</a>
</p>

---

## 💻 Sobre o Projeto

O **ActionCall** é uma solução corporativa (SaaS) desenvolvida para revolucionar operações de Contact Center. O sistema elimina planilhas manuais ao automatizar a distribuição de contatos para operadores, gerenciar status de ligações e calcular produtividade de forma descentralizada. 

*(Nota: Este é um projeto comercial com código-fonte mantido de forma estritamente confidencial/privada por questões de segurança e propriedade intelectual. Esta página atua como vitrine da arquitetura e das soluções técnicas adotadas.)*

## ✨ Funcionalidades Principais

* **Motor de Distribuição de Leads:** Algoritmo que "puxa" contatos de forma concorrente e segura utilizando a técnica transacional `FOR UPDATE SKIP LOCKED` no banco de dados, bloqueando qualquer risco de duplicidade de chamadas.
* **Importação Massiva:** Sistema de importação de planilhas complexas em lote, extraindo dados de forma inteligente (conversão estruturada em JSONB no Postgres).
* **Click-to-Call com VoIP SIP Nativo:** O sistema integra e aciona o softphone de VoIP (ex: MicroSIP) nativamente pelo próprio navegador, enviando o comando `sip:+55` com apenas um clique. Isso agiliza absurdamente o processo e zera o tempo de digitação, explodindo a produtividade do operador.
* **Filtros Dinâmicos Avançados:** Segmentação profunda e em tempo real por Município e Bairro dinamicamente extraídos das tabelas.
* **Módulo Financeiro:** Geração de relatórios analíticos formatados nativamente em arquivos do Excel (openpyxl), efetuando o cálculo diário do pagamento dos operadores com base em suas conversões.
* **Gestão Multinível:** Acesso isolado e compartimentado (Gestor, Admin, Operador).

## 🛠 Tecnologias e Arquitetura

O sistema foi arquitetado em backend para lidar com alta densidade de chamadas simultâneas sem perdas ou bloqueios (Deadlocks):

**Backend e Banco de Dados:**
- **Python 3** com **Flask**: Roteamento backend através de arquitetura WSGI leve e veloz.
- **PostgreSQL**: Banco de dados relacional (Single Source of Truth) utilizado por sua altíssima capacidade de concorrência.
- **JSONB**: Combinação estratégica das queries estruturadas do SQL com a maleabilidade NoSQL para importar colunas personalizadas.
- **Pandas** e **OpenPyXL**: Ciência e processamento veloz de listas de dados gigantes.

**Frontend UI/UX:**
- **Jinja2 + Vanilla JS**: Renderização de baixo custo misturada a ações reativas para velocidade extrema de navegação.
- **Tailwind CSS**: Uso de design pattern moderno com transparências, modais agradáveis (SweetAlerts) reduzindo o stress ocular do operador.

## 🚀 Demonstração do Projeto

Por ser um sistema corporativo privado de uso restrito, o ActionCall **não possui link público de testes aberto na internet**. 

A plataforma envolve dados de banco de dados e arquitetura complexa que rodam internamente para proteger a integridade das operações comerciais.

🤝 **Demonstração:** Caso seja um recrutador ou empresa interessada, fico inteiramente à disposição para agendar uma **chamada de vídeo rápida**, onde posso compartilhar a tela, rodar o ambiente de desenvolvimento localmente e mostrar todo o sistema, os códigos e a engenharia de software na prática!

---

<p align="center">
  Engenharia desenhada com foco em alta disponibilidade e prevenção de falhas de comunicação.
</p>
