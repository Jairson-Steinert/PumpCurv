# Histórico de Atualizações do Projeto

## 1. Objetivo

Este documento apresenta uma visão acadêmica da evolução do PumpCurv. As alterações foram consolidadas por período e área funcional para demonstrar o desenvolvimento do sistema sem divulgar código-fonte, rotas, configurações, mecanismos de segurança ou procedimentos internos.

- **Período documentado:** janeiro a junho de 2026
- **Última atualização considerada:** 19/06/2026
- **Autor:** Jairson Steinert

O registro técnico completo de commits permanece restrito ao repositório privado de desenvolvimento.

## 2. Janeiro e fevereiro de 2026 — Estruturação da solução

Nesta etapa foram estabelecidas as bases técnicas e funcionais do PumpCurv:

- organização inicial do frontend, backend e persistência;
- consulta de produtos e visualização de curvas hidráulicas;
- análise individual e comparação entre diferentes modelos;
- ajustes de rotação, diâmetro, potência e limites operacionais;
- implementação da seleção por ponto de operação;
- inclusão de tolerâncias e filtros para busca de alternativas;
- cálculos hidráulicos, NPSH, fator de serviço e conversões de unidades;
- autenticação, perfis de usuário e rastreabilidade das operações;
- geração de relatórios, impressão e exportação de dados;
- padronização dos componentes visuais e adaptação para dispositivos móveis.

## 3. Março de 2026 — Persistência e evolução da seleção

O sistema passou a oferecer maior continuidade e controle sobre os trabalhos:

- detecção de dimensionamentos semelhantes;
- composição de bombas em série e em paralelo;
- aperfeiçoamento da seleção por ponto e de seus filtros técnicos;
- tolerâncias assimétricas para o ponto solicitado;
- pré-visualização de curvas e produtos nos resultados;
- melhoria da persistência das sessões e dos estados de trabalho;
- maior consistência entre análise, comparação e relatórios;
- refinamentos de segurança, autorização e rastreabilidade.

## 4. Abril de 2026 — Seleção por aplicação

O escopo foi ampliado com novos fluxos orientados às características da aplicação:

- implementação do módulo de Seleção por Aplicação;
- assistentes para cenários residenciais e prediais;
- apoio a piscinas, irrigação, jardinagem e nebulização;
- suporte a cenários de combate a incêndio;
- cálculos de tubulações, perdas de carga e condições hidráulicas;
- diagnóstico de NPSH, margem disponível e risco de cavitação;
- mapeamento entre aplicações e linhas de produtos;
- melhorias nos gráficos, tabelas, filtros e documentos gerados;
- padronização da experiência entre os diferentes módulos.

## 5. Maio de 2026 — Colaboração e indicadores

As atualizações concentraram-se na gestão dos trabalhos e no acompanhamento do uso:

- controle de visibilidade de dimensionamentos e comparações;
- consulta de trabalhos públicos e solicitação de acesso a trabalhos privados;
- aprovação ou recusa de solicitações pelo proprietário;
- notificações associadas aos fluxos de acesso;
- criação do painel de dimensionamentos e indicadores administrativos;
- contabilização de impressões, reimpressões e comparações;
- exportação de indicadores e resultados para planilhas;
- refinamento dos filtros de rotor, sólidos, frequência e conexão;
- reformulação da página inicial e melhoria da experiência de navegação;
- padronização de relatórios e dados apresentados em tela.

## 6. Junho de 2026 — Consolidação e desempenho

O período final concentrou correções, desempenho e consistência dos resultados:

- otimização das consultas utilizadas na seleção de motobombas;
- melhoria da alternância entre produtos e identificadores de curvas;
- correções na associação entre produtos, curvas e dados de motor;
- atualização e revisão do catálogo técnico;
- melhoria da extrapolação e da representação do NPSH requerido;
- refinamento das tabelas hidráulicas e dos relatórios;
- ajustes para diferentes cenários de produto e aplicação;
- revisão de imagens, datasheets e informações apresentadas nos documentos;
- simplificação de fluxos e melhoria da legibilidade da interface.

## 7. Resultado da evolução

Ao final do período documentado, o PumpCurv passou a reunir em uma única plataforma:

- consulta de produtos e curvas;
- seleção por ponto de operação e por aplicação;
- dimensionamento e cálculos hidráulicos;
- análise e ajuste de curvas;
- comparação de alternativas;
- geração de relatórios e planilhas;
- salvamento, recuperação e compartilhamento controlado de trabalhos;
- indicadores de uso, auditoria e rastreabilidade.

Entre 18 de março e 19 de junho de 2026 foram registrados 180 commits no repositório privado, distribuídos da seguinte forma:

| Mês | Commits |
|---|---:|
| Março de 2026 | 35 |
| Abril de 2026 | 75 |
| Maio de 2026 | 49 |
| Junho de 2026 | 21 |
| **Total** | **180** |

## 8. Limites de publicação

Esta versão não apresenta:

- hashes ou mensagens técnicas completas de commits;
- nomes de rotas, endpoints ou contratos internos;
- parâmetros e mecanismos de autenticação ou sessão;
- caminhos de arquivos, bancos de dados ou infraestrutura;
- configurações, credenciais, segredos ou procedimentos operacionais;
- nomes de arquivos e componentes do código-fonte.

*Fonte: Elaborado pelo autor com base no histórico privado do projeto.*
