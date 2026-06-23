# Proposta de Projeto — PumpCurv

## Proposta (Contexto, Objetivo, Justificativa, Diferencial e Resultado Esperado)

A seleção de bombas hidráulicas em projetos de engenharia exige a análise de curvas de desempenho, a comparação entre diferentes modelos e a validação de pontos de operação conforme normas técnicas como NFPA 20 e NBR 16704. Atualmente, esse processo é realizado de forma manual com planilhas e catálogos em papel, o que consome tempo, está sujeito a erros de interpretação e dificulta a padronização dos resultados entre profissionais. O objetivo deste projeto é desenvolver uma aplicação web capaz de centralizar a visualização de curvas de bomba, a busca automática por ponto de operação com tolerâncias configuráveis, a comparação simultânea de múltiplos modelos com ranking por eficiência e potência, e a geração de relatórios técnicos em PDF. A justificativa se apoia na necessidade de reduzir o tempo de análise e aumentar a confiabilidade das decisões de engenharia, oferecendo consistência nos cálculos hidráulicos e rastreabilidade por meio de registro de auditoria. O diferencial da solução está na integração de interpolação polinomial por segmentos, cálculo de NPSH disponível com propriedades termodinâmicas de fluidos, aplicação das leis de afinidade para ajuste de rotação e diâmetro de rotor, e detecção automática de dimensionamentos similares já realizados, tudo em uma única interface responsiva com autenticação e controle de acesso. Como resultado esperado, a aplicação permitirá que engenheiros realizem seleções de bomba de forma mais rápida, fundamentada e documentada, com exportação direta de dados para Excel e impressão de laudos técnicos padronizados.

---

## Cronograma de Execução

O projeto teve início em janeiro de 2026. O cronograma foi atualizado em 22 de junho de 2026 com base nas atividades efetivamente realizadas, no histórico de evolução do sistema e nos próximos passos definidos no RFC. As adequações de escopo ocorridas durante o desenvolvimento foram validadas com o professor orientador e com a Famac Ind. de Máquinas Ltd.

| Período | Etapa | Principais entregas | Situação em 22/06/2026 |
|---|---|---|---|
| Janeiro de 2026 | Estruturação da solução | Organização do frontend, backend e persistência; consulta de produtos; visualização inicial das curvas; cálculos e comparação de modelos. | Concluída |
| Fevereiro de 2026 | Consolidação dos módulos iniciais | Seleção por ponto de operação; tolerâncias e filtros; ajustes de curvas; NPSH; fator de serviço; autenticação; relatórios e padronização da interface. | Concluída |
| Março de 2026 | Persistência e evolução da seleção | Salvamento e recuperação de trabalhos; detecção de dimensionamentos semelhantes; bombas em série e paralelo; refinamento dos filtros e da rastreabilidade. | Concluída |
| Abril de 2026 | Seleção por aplicação | Assistentes hidráulicos para diferentes aplicações; cálculos de tubulações e perdas; diagnóstico de NPSH; mapeamento de linhas e melhoria dos relatórios. | Concluída |
| Maio de 2026 | Colaboração e indicadores | Visibilidade de trabalhos; solicitações de acesso; notificações; painel de dimensionamentos; indicadores; exportação de dados e melhorias de usabilidade. | Concluída |
| Junho de 2026 | Consolidação e documentação | Otimização das consultas; revisão do catálogo; correções hidráulicas; consistência entre tela e relatórios; testes; RFC; arquitetura; banner e documentação acadêmica. | Em andamento |
| Julho de 2026 | Encerramento acadêmico e implantação assistida | Validação final com usuários; correções de regressão; preparação do ambiente; treinamento; apresentação e ajustes finais da documentação. | Prevista |

### Situação atual

Os módulos centrais de consulta, seleção por ponto, seleção por aplicação, dimensionamento, comparação, relatórios, autenticação, auditoria e administração estão implementados. Em junho, o trabalho concentra-se na validação dos resultados, na consistência dos dados, no desempenho, na experiência do usuário e na finalização da documentação acadêmica.

### Atividades finais priorizadas

1. concluir os testes hidráulicos e de regressão;
2. validar resultados e relatórios com usuários finais;
3. corrigir inconsistências remanescentes entre produtos e curvas;
4. concluir a documentação acadêmica e operacional autorizada;
5. preparar a implantação assistida e o treinamento dos usuários;
6. consolidar o feedback obtido na fase inicial de utilização;
7. realizar a apresentação e as correções finais do projeto.
