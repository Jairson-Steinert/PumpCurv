# Arquitetura do Sistema — PumpCurv

## 1. Objetivo

Este documento apresenta a arquitetura atual do PumpCurv em nível acadêmico e funcional. A descrição abrange tecnologias, camadas, módulos, diretórios, responsabilidades e fluxos principais, sem divulgar o código-fonte ou detalhes que possam comprometer a segurança da aplicação.

O PumpCurv é uma aplicação web interna destinada à consulta, análise, dimensionamento e seleção de motobombas. A solução centraliza dados técnicos, curvas de desempenho, cálculos hidráulicos, comparação de alternativas, emissão de relatórios e rastreabilidade dos trabalhos realizados.

## 2. Visão arquitetural

A solução segue uma arquitetura cliente-servidor organizada em três áreas principais:

1. **frontend:** interface web, gráficos, formulários e fluxos de interação;
2. **backend:** API, validações, cálculos e regras de negócio;
3. **dados e segurança:** persistência, autenticação, autorização, auditoria e integridade das informações.

O usuário interage com o frontend web, responsável por coletar os dados, apresentar os módulos e exibir os resultados. A interface encaminha as solicitações à API REST, que valida as informações e direciona cada operação aos serviços correspondentes. Esses serviços executam os cálculos e as regras de negócio e utilizam a camada de persistência para consultar ou registrar os dados necessários. Essa separação impede o acesso direto da interface ao banco de dados e mantém as regras técnicas independentes da forma como os resultados são apresentados.

## 3. Tecnologias principais

| Área | Tecnologias | Finalidade |
|---|---|---|
| Frontend | React, TypeScript e Vite | Construção da interface web e organização dos módulos visuais. |
| Estilização | Tailwind CSS | Padronização visual e responsividade. |
| Gráficos | Recharts e Plotly.js | Visualização e interação com curvas e indicadores. |
| Comunicação | API REST | Troca de dados entre frontend e backend. |
| Backend | Python, FastAPI e Pydantic | Processamento, validação e exposição dos casos de uso. |
| Servidor de aplicação | Uvicorn | Execução da aplicação backend. |
| Persistência | SQLAlchemy e SQLite | Mapeamento e armazenamento relacional dos dados. |
| Segurança | Autenticação, autorização e proteção de sessão | Restrição de acesso e rastreabilidade das operações. |

As versões, configurações e parâmetros internos dessas tecnologias não fazem parte da documentação de entrega.

## 4. Componentes da solução

### 4.1. Frontend

O frontend concentra a experiência do usuário. Suas responsabilidades incluem:

- apresentar produtos, curvas e resultados hidráulicos;
- coletar dados de entrada e aplicar validações de interface;
- exibir gráficos, tabelas, comparações e indicadores;
- conduzir os fluxos de seleção por ponto e por aplicação;
- organizar ajustes de curvas e configurações de dimensionamento;
- solicitar ao backend cálculos, consultas, salvamentos e exportações;
- apresentar recursos conforme o perfil e as permissões do usuário.

### 4.2. Backend

O backend centraliza o processamento e as regras de negócio. Suas responsabilidades incluem:

- validar solicitações recebidas da interface;
- consultar produtos, curvas e mapeamentos técnicos;
- executar cálculos hidráulicos e avaliações de desempenho;
- aplicar filtros, tolerâncias e regras de classificação;
- coordenar dimensionamentos, comparações e revisões;
- controlar acesso, autoria, visibilidade e ciclo de vida dos trabalhos;
- produzir dados para relatórios, planilhas e indicadores;
- registrar operações relevantes para auditoria e rastreabilidade.

### 4.3. Persistência

A camada de persistência mantém os dados necessários ao funcionamento do sistema. Em nível lógico, eles estão organizados nos seguintes grupos:

- usuários, perfis, sessões e solicitações de acesso;
- produtos, linhas, aplicações e respectivos mapeamentos;
- curvas de bomba e equações segmentadas;
- dimensionamentos, resultados e trabalhos salvos;
- comparações, revisões e estados persistidos;
- impressões, atividades, indicadores e registros de auditoria.

Detalhes como nomes físicos de tabelas, campos internos, índices e caminhos de armazenamento não são expostos nesta documentação.

## 5. Estrutura de diretórios

```text
PumpCurv/
├── src/                         # aplicação frontend
│   ├── components/              # componentes visuais e módulos funcionais
│   │   ├── admin/               # recursos administrativos
│   │   ├── applicationSelection/ # seleção por aplicação
│   │   ├── comparison/          # comparação de curvas e alternativas
│   │   ├── pdf/                 # composição dos documentos gerados
│   │   ├── pointSelection/      # seleção por ponto de operação
│   │   ├── ui/                  # componentes reutilizáveis de interface
│   │   └── user/                # recursos relacionados ao usuário
│   ├── constants/               # constantes compartilhadas
│   ├── contexts/                # estados globais e contextos da aplicação
│   ├── hooks/                   # comportamentos reutilizáveis da interface
│   ├── services/                # comunicação do frontend com a API
│   ├── types/                   # contratos e tipos compartilhados
│   └── utils/                   # cálculos, conversões e formatações auxiliares
├── public/
│   └── images/                  # imagens e recursos estáticos da interface
├── backend/                     # aplicação backend
│   ├── api/
│   │   ├── routes/              # pontos de entrada das funcionalidades
│   │   └── schemas/             # contratos de entrada e saída de dados
│   ├── importers/               # importação controlada de dados técnicos
│   ├── middleware/              # controles transversais de requisição
│   ├── models/                  # representação das entidades persistidas
│   ├── repositories/            # acesso e consulta aos dados
│   └── services/                # regras de negócio e serviços de aplicação
├── scripts/                     # rotinas internas de preparação e manutenção
├── documentacao/                # documentação técnica mantida com o projeto
└── entrega-documentacao/        # documentação acadêmica destinada à entrega
```

Diretórios de dependências, ambientes virtuais, caches, artefatos de compilação e arquivos temporários foram omitidos por não representarem partes lógicas da solução. Já os arquivos de configuração, dados privados, procedimentos operacionais e outros elementos internos foram omitidos por questões de sigilo, conforme estabelecido no RFC. Essa restrição atende ao interesse da Famac Ind. de Máquinas Ltd. em preservar o código-fonte e os detalhes internos do sistema e foi validada com o professor orientador.

| Diretório | Responsabilidade principal |
|---|---|
| `src` | Interface, módulos funcionais, gráficos e interação com o usuário. |
| `public` | Imagens e recursos estáticos utilizados pela interface. |
| `backend` | API, validações, cálculos, regras de negócio e persistência. |
| `scripts` | Rotinas internas e controladas de preparação e manutenção. |
| `documentacao` | Registros técnicos mantidos junto ao projeto privado. |
| `entrega-documentacao` | Documentos autorizados para avaliação acadêmica. |

## 6. Organização do frontend

O frontend combina organização por funcionalidade e por responsabilidade técnica.

### 6.1. Módulos funcionais

- **seleção por ponto:** recebe vazão, altura manométrica, tolerâncias e filtros para localizar alternativas compatíveis;
- **seleção por aplicação:** conduz assistentes hidráulicos de acordo com o cenário informado;
- **comparação:** reúne curvas e dados técnicos de diferentes alternativas;
- **análise e ajuste:** permite avaliar curvas e simular ajustes admitidos pelo sistema;
- **documentos:** compõe relatórios e representações adequadas à impressão;
- **administração:** apresenta indicadores e funções restritas de gerenciamento;
- **usuário:** organiza conta, histórico, trabalhos e solicitações de acesso.

### 6.2. Elementos compartilhados

- componentes de interface reutilizáveis;
- contextos para estados globais e identidade do usuário;
- hooks para comportamentos repetidos;
- serviços para comunicação com a API;
- tipos para contratos internos do frontend;
- utilitários para conversões, cálculos auxiliares e formatação.

## 7. Organização do backend

O backend segue uma divisão em camadas:

1. **API e schemas:** recebem solicitações e validam os contratos de dados;
2. **serviços:** executam casos de uso, cálculos e regras de negócio;
3. **repositórios:** isolam as operações de consulta e persistência;
4. **modelos:** representam as entidades armazenadas;
5. **middleware:** aplica controles comuns às requisições;
6. **importadores:** normalizam a entrada controlada de dados técnicos.

Os scripts administrativos permanecem separados do fluxo normal da aplicação, pois atendem a rotinas controladas de preparação e manutenção.

## 8. Fluxos funcionais principais

### 8.1. Consulta e análise de produto

```text
Consulta do usuário
   → localização do produto e de suas curvas
   → carregamento dos dados técnicos
   → visualização e análise gráfica
   → geração ou salvamento do resultado
```

### 8.2. Seleção por ponto de operação

```text
Vazão, altura e filtros
   → identificação das curvas elegíveis
   → avaliação das equações segmentadas
   → aplicação de tolerâncias e critérios técnicos
   → classificação das alternativas
   → análise, comparação ou relatório
```

### 8.3. Seleção por aplicação

```text
Características da aplicação
   → definição das condições hidráulicas
   → cálculo do ponto requerido
   → mapeamento das linhas de produtos
   → seleção das alternativas compatíveis
   → apresentação dos resultados
```

### 8.4. Comparação e documentação

```text
Alternativas selecionadas
   → padronização das grandezas
   → comparação gráfica e tabular
   → registro da revisão
   → geração de relatório ou planilha
```

### 8.5. Trabalhos e controle de acesso

```text
Trabalho salvo
   → definição de autoria e visibilidade
   → consulta ou solicitação de acesso
   → decisão do proprietário quando necessária
   → registro da operação e notificação
```

## 9. Regras de dependência

As dependências devem seguir preferencialmente a direção abaixo:

```text
Componentes de interface
   → serviços do frontend
   → API do backend
   → serviços de aplicação
   → repositórios e modelos
   → persistência
```

São adotadas as seguintes restrições arquiteturais:

- componentes visuais não acessam diretamente o banco de dados;
- regras centrais de negócio não dependem da representação visual;
- repositórios não assumem responsabilidades de interface;
- importações e manutenções não integram o fluxo comum dos usuários;
- permissões são verificadas no backend, independentemente da visibilidade dos controles no frontend.

## 10. Qualidades arquiteturais

### 10.1. Manutenibilidade

A separação entre módulos e camadas permite localizar responsabilidades, reduzir duplicações e alterar uma área com menor impacto sobre as demais.

### 10.2. Rastreabilidade

Trabalhos, revisões, impressões e atividades relevantes podem ser associados à autoria e ao contexto em que foram realizados.

### 10.3. Consistência

As regras técnicas e os cálculos são centralizados, reduzindo divergências entre usuários e documentos gerados.

### 10.4. Desempenho

Consultas, processamento de curvas e renderização gráfica são organizados para evitar operações redundantes e manter resposta adequada nos principais fluxos.

### 10.5. Evolução

A modularidade permite incorporar novas aplicações, linhas de produtos, critérios hidráulicos e formas de visualização sem exigir a substituição integral da solução.

### 10.6. Segurança

A aplicação aplica autenticação, autorização por perfil, proteção de sessão, validação das entradas e auditoria de operações relevantes. Esta documentação registra apenas esses objetivos; os mecanismos, parâmetros e configurações internos permanecem restritos.

## 11. Visão de implantação

Em produção, o usuário acessa a aplicação por meio de um navegador. A interface comunica-se com o backend, que processa as regras e acessa a persistência. Os detalhes físicos de hospedagem, rede e configuração não são publicados.

```text
Navegador
   → aplicação web
   → serviço backend
   → armazenamento persistente
```

## 12. Limites desta documentação

Por segurança e confidencialidade, este documento não apresenta:

- rotas, endpoints ou formatos completos de requisição;
- portas, domínios, endereços e topologia de rede;
- credenciais, chaves, tokens, certificados ou segredos;
- arquivos e variáveis de ambiente;
- caminhos físicos de bancos, catálogos ou diretórios corporativos;
- parâmetros de sessão, políticas internas ou detalhes dos mecanismos de proteção;
- esquemas físicos completos de persistência;
- scripts operacionais e instruções de implantação;
- trechos ou arquivos do código-fonte.

## 13. Relação com os demais documentos

- o [RFC](RFC.md) registra requisitos, decisões, cálculos, arquitetura acadêmica e evolução do escopo;
- a seção **Estrutura de diretórios** deste documento registra a organização lógica das pastas;
- o histórico de atualizações registra a evolução cronológica do sistema;
- a proposta do projeto preserva o contexto e o planejamento iniciais.

*Fonte: Elaborado pelo autor.*
