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

## Relatório para o professor com quatro gráficos

O [entregável em PDF](entrega/entregavel.pdf) usa a versão revisada fornecida pelo grupo, agora com onze páginas após os complementos de limites e derivadas. Mantém fonte Liberation Sans de 12 pontos, títulos e subtítulos em negrito, figuras de ocupação, derivada, integral e histórico e fórmulas em notação matemática. O [GeoGebra correspondente](entrega/S01_quatro_graficos.ggb), com o layout corrigido, acompanha esse relatório.

O PDF contém os nomes e RMs registrados no contexto do projeto. Os dados continuam simulados. A finalização das páginas 2 e 3 está em `apoio/finalizar_pdf_anexado.py`, baseada no anexo preservado em `apoio/temporarios/finalizacao_anexo_20261113/original_anexado.pdf`. O complemento de 14/11 está em `apoio/incorporar_complemento.py`: acrescenta os limites laterais na página 4, insere a demonstração das derivadas e máximos dos Dias 2 e 3 na página 7 e renumera as páginas seguintes. O gerador `apoio/gerar_entregavel.py` corresponde à versão anterior de nove páginas e não deve ser usado para sobrescrever o PDF final.

O relatório usa fundo branco e escrita preta, com títulos e subtítulos em negrito. Não há tabelas ou fundos decorativos: integrantes, RMs, registros e comparações estão em parágrafos. As figuras estão em preto e branco; a área da integral é identificada por hachuras.

Na finalização, a descrição passou a apresentar a Study Comfort, o Supabase e a análise restrita à ocupação da S01 com dados fictícios. A frase sobre a escolha dos registros para coincidir com as parábolas foi retirada da página 2. A página 3 explicita a forma geral da função do segundo grau e o papel de cada coeficiente. As outras oito páginas do anexo foram preservadas integralmente. A última seção continua sendo **Resultados e aplicação**; os cálculos dos três dias foram conferidos.

O [ZIP de envio ao professor](entrega/entrega_math.zip) contém **somente dois arquivos**, na raiz: `entregavel.pdf` e `S01_quatro_graficos.ggb`. Documentação de apoio, geradores, dados separados, versões anteriores e temporários não integram esse pacote.

## Versão simplificada preservada

A versão simplificada anterior usa **um dia simulado e um único gráfico de ocupação**, com registros de 3 em 3 horas, das 06h às 21h. Limite, derivada e integral são explicados usando essa mesma curva. Não há seletores, gráfico separado de derivada, tela separada de integral ou histórico.

## Arquivos para usar

- [Abrir o GeoGebra anterior](apoio/versoes_anteriores/20261113_limpeza_entrega/S01_calculo_3h.ggb): os seis registros, a curva, o máximo estimado e a área acumulada no mesmo gráfico.
- [Ler a explicação simples anterior em PDF](apoio/versoes_anteriores/20261113_limpeza_entrega/relatorio_calculo_S01.pdf): cinco páginas com variáveis, interpretação, contas e roteiro de apresentação.
- [Passo a passo em texto](documentacao/PASSO_A_PASSO.md).
- [Relação com as listas do ano](documentacao/ALINHAMENTO_ANO.md).

Os arquivos desta seção simplificada permanecem preservados localmente, mas não integram o ZIP de envio ao professor. Não é necessário executar Python para abrir GGB ou PDF.

## Resultados do exemplo

Registros: 1, 5, 7, 7, 5 e 1 pessoas, respectivamente às 06h, 09h, 12h, 15h, 18h e 21h. Capacidade adotada: 9 pessoas.

Modelo: `N(x) = -x²/9 + 3x - 13`, apenas em `[6,21]`. Maior registro: 7 pessoas às 12h e às 15h. Máximo estimado da curva: 7,25 às 13h30. Limite em 12h: 7. Área no dia: 77,5 pessoa-horas. Média temporal do modelo: aproximadamente 5,17 pessoas.

Os dados são fictícios e foram escolhidos para combinar com a função. A área não conta visitantes distintos. As leituras de 3h podem perder picos; um único dia não estabelece horários habituais de maior movimento. Não há coleta automática nem publicação diária no site.

## Reproduzir

Requer Python 3.10+, ReportLab e fontes Arial do Windows:

```powershell
python -m pip install reportlab
python .\apoio\gerar_entrega.py
```

O gerador usa caminhos relativos ao próprio arquivo e a captura `apoio/evidencias_ano/01_ocupacao.png`, já incluída. Grava GGB e PDF em `entrega/`, e CSV, JSON e XML em `apoio/`. O ZIP é preparado separadamente; não se atualiza sozinho. Editar apenas o CSV não altera a curva; os coeficientes e textos estão no gerador.

## Versões guardadas

A versão anterior, com os quatro modos e os dois PDFs, está no arquivo externo `../versão_antiga.zip`. A primeira solução complexa continua separada em `../solucao_complexa.zip`. Nenhum desses arquivos integra o pacote atual ou é necessário para abri-lo.

Os materiais completos das aulas e os temporários permanecem somente no apoio local, fora do ZIP. A equipe deve conferir sua identificação e a rubrica do professor antes de submeter. Nenhuma submissão foi feita.
