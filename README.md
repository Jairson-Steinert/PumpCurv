# PumpCurv — Documentação Acadêmica

Este repositório reúne exclusivamente a documentação acadêmica do **PumpCurv — Sistema de Seleção e Curvas de Bombas**. Ele não corresponde ao repositório de desenvolvimento da aplicação e não contém seu código-fonte.

O projeto foi desenvolvido no curso de **Bacharelado em Engenharia de Software da Católica de Santa Catarina**, por **Jairson Steinert**, sob orientação do **Prof. Dr. Andrei Carniel**, em colaboração com a **Famac Ind. de Máquinas Ltd.**

## Sobre o projeto

O PumpCurv é uma aplicação web interna destinada a apoiar a consulta, a análise e a seleção de motobombas. A solução centraliza dados técnicos, curvas de desempenho, cálculos hidráulicos e trabalhos realizados, reduzindo a dependência de planilhas isoladas e favorecendo a padronização e a rastreabilidade das atividades.

Em uma visão de alto nível, a solução está organizada em três áreas:

- **interface e visualização**, responsável pela interação com o usuário e pela apresentação das curvas;
- **processamento e regras de negócio**, responsável pelos cálculos, filtros e classificações;
- **dados e segurança**, responsável pela persistência, autenticação, autorização e rastreabilidade.

Os detalhes acadêmicos sobre requisitos, arquitetura, tecnologias, critérios técnicos e evolução do projeto estão consolidados no RFC.

## Documentos

- [RFC — PumpCurv: Sistema de Seleção e Curvas de Bombas](RFC.md) — especificação atual e documento principal;
- [Arquitetura do sistema](ARQUITETURA.md) — visão atual das camadas, componentes, tecnologias e fluxos funcionais;
- [Proposta inicial do projeto](PROPOSTA_PROJETO.md) — registro acadêmico da concepção e do planejamento inicial;
- [Histórico de atualizações](Histórico_Atualizações_Projeto.md) — evolução cronológica do projeto com base nos commits registrados;
- [Telas do sistema](TELAS_DO_SISTEMA.md) — apresentação visual dos principais módulos e fluxos da aplicação.

Em caso de divergência entre os documentos, prevalece o RFC, que registra o escopo efetivamente desenvolvido e as alterações posteriormente aprovadas.

## Requisitos Funcionais e Não Funcionais do Sistema

- [RF](RFC.md#31-rf);
- [RNF](RFC.md#32-rnf).

## Diagramas e materiais visuais

Os diagramas estão incorporados e contextualizados no RFC. Os principais materiais são:

- [Diagrama de casos de uso](img/Diagrama_caso_uso.jpg);
- [Diagrama de contexto — C4 Nível 1](img/c4_nivel1_contexto_pumpcurv.png);
- [Diagrama de contêineres — C4 Nível 2](img/c4_nivel2_conteineres.png);
- [Componentes do frontend — C4 Nível 3](img/c4_nivel3_componentes_front.png);
- [Componentes do backend — C4 Nível 3](img/c4_nivel3_compnentes_backend.png);
- [Tecnologias e arquitetura](img/Tecnologias.png).

## Estrutura da entrega

```text
/
├── README.md          # apresentação e navegação da documentação
├── RFC.md             # documento acadêmico principal
├── ARQUITETURA.md     # visão arquitetural sanitizada do sistema
├── PROPOSTA_PROJETO.md # proposta e planejamento iniciais
├── Histórico_Atualizações_Projeto.md # histórico de evolução do projeto
├── TELAS_DO_SISTEMA.md # galeria das principais telas da aplicação
├── img/               # figuras utilizadas nos documentos
└── arquivo_pdf/       # exemplos de relatórios gerados pela aplicação
```

## Confidencialidade e propriedade intelectual

Por decisão da **Famac Ind. de Máquinas Ltd.**, validada com o professor orientador, o código-fonte e o repositório de desenvolvimento do PumpCurv são mantidos sob sigilo por envolverem interesses técnicos e comerciais da empresa.

Por esse motivo, esta entrega não inclui:

- código-fonte, executáveis ou pacotes da aplicação;
- credenciais, chaves, tokens ou variáveis de ambiente;
- bancos de dados, registros de auditoria ou dados pessoais;
- endereços de infraestrutura, rotas internas ou instruções de implantação;
- esquemas detalhados de persistência e configurações de segurança;
- scripts de importação, migração ou manutenção;
- documentos operacionais internos e dados técnicos proprietários.

A disponibilização desta documentação tem finalidade acadêmica e não concede acesso, licença ou autorização de uso do código-fonte. O PumpCurv não é apresentado como projeto de código aberto.

## Critérios para publicação

Antes de enviar uma atualização ao repositório acadêmico, deve-se confirmar que:

- o conteúdo pertence ao escopo acadêmico aprovado;
- nenhum trecho de código ou detalhe interno foi incluído;
- imagens e exemplos não exibem dados pessoais ou corporativos restritos;
- os links utilizam apenas arquivos presentes nesta entrega;
- as figuras possuem título, fonte e legibilidade adequados;
- o RFC e este índice permanecem coerentes entre si.

## Contato acadêmico

**Jairson Steinert**  
Graduando do curso de Bacharelado em Engenharia de Software — Católica de Santa Catarina  
[j.steinert@catolicasc.edu.br](mailto:j.steinert@catolicasc.edu.br)
