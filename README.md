# Matemática - S01

## Ficha CitizenTech

| Campo | Definição |
|---|---|
| Nome da solução | Study Comfort. |
| Cidade e bairro | São Paulo/SP |
| Cidadão beneficiado | Estudantes universitários que querem escolher um ambiente adequado para estudar, trabalhar em grupo ou gravar vídeos/projetos. |
| Problema em uma frase | Estudantes têm dificuldade para identificar, antes de se deslocar, salas com espaço e condições adequadas de ruído, temperatura e luminosidade para suas atividades. |
| Como funciona | O fluxo da S01 (Sala 1) é ESP32 simulado no Wokwi → Supabase → painel React. A conexão local está configurada e a leitura pelo painel foi validada. S02 a S09 usam simulações locais. O painel oferece filtros, recomendações, favoritos locais e listas compartilhadas no Supabase. |
| O que cada parte faz | Edge: leitura simulada e decisão local (LEDs); Supabase: guarda o histórico da sala IoT e as listas compartilhadas; React/Web: exibição, filtros, rankings e CRUD de listas pela API.
| Repositório | https://github.com/JeckyCossio/study-comfort (público) |
| Indicador de impacto | Novas entrevistas com os usuários da plataforma, perguntando quanto tempo provavelmente foi economizado através do uso da plataforma, e quantas vezes por seman é usado a plataforma pelo usuário |
| ODS conectados | ODS 4: Educação de Qualidade (principal: melhores condições para estudar); ODS 9: Indústria, Inovação e Infraestrutura (apoio: IoT aplicada à infraestrutura do campus); possivelmente ODS 11: Cidades e Comunidades Sustentáveis (uso eficiente de espaços coletivos). |

### Equipe

| Integrante | RM |
|---|---|
| Daniel Roberto | 571746 |
| Felipe Pedrol | 569631 |
| Jecky Cossio | 572226 |
| Felipi Godoy | 573741 |

## Sobre a entrega

Trabalho de Cálculo da Global Solution CitizenTech 2026.2, relacionado à solução Study Comfort. A análise considera a ocupação da sala S01, com capacidade de nove pessoas, em três dias simulados, no intervalo de 06h a 21h.

O relatório apresenta modelos quadráticos, limites, derivadas, máximos, integrais e comparação histórica. O arquivo GeoGebra acompanha a análise com quatro visualizações: ocupação, derivada, integral e histórico.

## Materiais presentes no repositório

| Arquivo | Conteúdo |
| --- | --- |
| [entregavel.pdf](entrega/entregavel.pdf) | Relatório final de 11 páginas com identificação da equipe, modelos, cálculos, quatro gráficos e interpretação dos resultados. |
| [S01_quatro_graficos.ggb](entrega/S01_quatro_graficos.ggb) | Arquivo GeoGebra correspondente ao relatório, para explorar as visualizações e os cenários simulados. |
| [entrega_math.zip](entrega/entrega_math.zip) | Pacote de entrega com o PDF e o arquivo GeoGebra na raiz. |

## Como consultar

1. Abra ou baixe o [relatório em PDF](entrega/entregavel.pdf) para acompanhar as explicações e os cálculos.
2. Baixe o [arquivo GGB](entrega/S01_quatro_graficos.ggb) e abra no GeoGebra. Consulte as orientações do relatório para explorar os quatro modos.
3. Para obter os dois materiais juntos, baixe e extraia o [ZIP da entrega](entrega/entrega_math.zip).

Não é necessário executar Python para consultar o PDF ou abrir o GeoGebra.

## O que é analisado

- **Modelo matemático:** funções quadráticas para representar os três cenários diários de ocupação.
- **Limites:** comportamento das funções próximo de um horário, incluindo limites laterais.
- **Ocupação e máximo:** comparação com a capacidade da sala e estimativa do horário de pico.
- **Derivada:** taxas de crescimento e diminuição da ocupação e identificação dos máximos.
- **Integral:** uso acumulado em pessoa-hora e comparação entre períodos e dias.
- **Histórico:** médias dos registros dos três dias para comparar horários.

## Interpretação dos dados

Os dados são fictícios e servem à demonstração acadêmica. A análise de Cálculo não utiliza medições físicas de uma sala nem representa uma coleta automática de dados do Wokwi.

As curvas estimam a ocupação entre os registros e podem assumir valores fracionários. A integral representa uso acumulado em pessoa-hora, não a quantidade de visitantes distintos. Três dias simulados não comprovam um padrão real de utilização; as conclusões ficam restritas aos cenários apresentados.

## Estrutura do repositório

```text
README.md
entrega/
├── entregavel.pdf
├── S01_quatro_graficos.ggb
└── entrega_math.zip
```

## Pacote para entrega

O arquivo `entrega/entrega_math.zip` contém somente:

```text
entregavel.pdf
S01_quatro_graficos.ggb
```

Os arquivos dentro do ZIP correspondem às versões disponíveis separadamente na pasta `entrega`.
