# Comparação de Ferramentas de Extração Texto voltadas para o contexto jurídico
Repositório da Task para Avaliar ferramentas de Extração de Texto
 #### Ferramentas Usadas
  
| Ferramenta | Abordagem | 
|    :---:   |     :---:     |  
|  Pytesseract|   OCR |   
|  PDFX|   TS   |    
| PyMuPDF| TS |
| PyPdf2| TS |

 #### Documentos Usados para a 1ª Base de Dados

| Dataset|   Documento |    Link      | Nº de Paginas |
| :---:  |    :---:    |     :---:    |  :---:        |
|Dataset 1 |  Notes on the Paranormal by Ben Steigmann| https://encurtador.com.br/fgLPX |  185 |
|Dataset 2 |  Diálogo entre a sociologia e a psicanálise: o indivíduo e o sujeito by SciELO - EDUFBA | https://encurtador.com.br/cmPU2  | 287|
|Dataset 3| Iracema (Versão original) by José de Alencar     |   https://encurtador.com.br/bdgmD  |  143 |   
|Dataset 4|  O Paraíso Perdido, John Milton ( Ediouro) - John Milton's Paradise Lost: A Literal translation for portuguese in prose text by Ediouro, John Milton, Conceição G. Sotto Maior  | https://encurtador.com.br/cdz45    |   261 |
| Dataset 5| Histórias e Tradições da Cidade de Sao Paulo by Ernani Silva Bruno     |  https://encurtador.com.br/hkoGW   |  686|
       

 #### Resultados do Tempo
  
| Ferramenta | Tempo em segundos| 
|    :---:   |  :---:    |  
|   Pytesseract |     4085,82     | 
|   PDFX    |       49,07    |  
|   PyMuPDF   |      2,58    |    
|   PyPdf2  |       76,38   |  




 #### Taxa de Erro de Caractere (CER)
  
| Ferramenta  | Dataset 1 |Dataset 2 |Dataset 3 |Dataset 4 |Dataset 5  |Desvio Padrão  | Média |
|    :---:    |  :---:    |   :---:   | :---:    | :---:    | :---:    | :---:         | :---: |
| Pytesseract | 2,15%     |  5,43%    |  5,13%   | 11,29%   |  27,55%  | $$\pm$$ 10,19 | 10,31 %|
| PDFX        | 8,41%     | 9,13%     | 11,97%   | 3,96%    | 3,76%    | $$\pm$$ 3,53  | 7,44%  |
| PyMuPDF     |  1,97%    |  2,11%    | 5,06%    |  4,07%   | 0,8%     | $$\pm$$ 1,72  | 2,80%  |
| PyPdf2      | 2,05%     |  5,91%    | 4,86%    | 11,52%   | 1,97%    | $$\pm$$ 3,90  | 5,26%  |



 #### Taxa de Erro de Palavras (WER)
  
| Ferramenta  | Dataset 1 |Dataset 2 |Dataset 3 |Dataset 4 |Dataset 5 |Desvio Padrão  | Média  |
|    :---:    |  :---:    |   :---:   | :---:    | :---:   | :---:    | :---:         | :---:  |
| Pytesseract | 18,14%    | 32,03%    |27,74%    | 36,32%  | 46,24%   | $$\pm$$ 10.38 | 32,09% |
| PDFX        | 6,67%     | 11%       |18,42%    | 7,38%   | 3,82%    | $$\pm$$ 5.62  | 9,45%  |
| PyMuPDF     |8,12%      | 8,94%     | 25,90%   | 9,79%   | 0,34%    | $$\pm$$ 9.34  | 10,61% |
| PyPdf2      | 8,14%     | 11,51%    |  25,95%  | 9,90%   | 0,33%    | $$\pm$$ 9.31  | 11,16% |

## Discussão

Quando se trata de precisão do OCR, duas métricas objetivas são usadas para avaliar o quão confiável é o OCR: Taxa de erros de caracteres (CER) e Taxa de erros de palavras (WER).
O cálculo do CER é baseado no conceito de distância de Levenshtein, onde contamos o número mínimo de operações em nível de caractere necessárias para transformar o texto verdadeiro na saída de OCR.
Um artigo publicado em 2009 sobre a revisão da precisão do OCR em programas de digitalização de jornais australianos em grande escala apresentou estes benchmarks (para texto impresso )[1]:

- Boa precisão de OCR: CER 1-2% (ou seja, 98-99% de precisão)
- Precisão média de OCR: CER 2-10%
- Baixa precisão do OCR: CER > 10% (ou seja, abaixo de 90% de precisão)

O cálculo do WER também é baseado no conceito de distância de Levenshtein, onde contamos o número mínimo de operações em nível de palavra necessárias para transformar o texto verdadeiro na saída de OCR.
O WER está geralmente bem correlacionado com o CER (desde que as taxas de erro não sejam excessivamente altas), embora se espere que o valor absoluto do WER seja superior ao valor do CER[1].

## Conclusão 

A partir dos Resultados dos Experimentos, a Ferramenta PyMuPDF obteve as melhores metricas, sendo extremamente rápida em seu tempo total na extração de todos os documentos , e tendo as menores médias e desvio padrão de erro CER ,tendo uma precisão de 97,80%. 

## Referência
[1] TIMALSINA, AMIT.Analysis and Benchmarking of OCR Accuracy for Data Extraction Models.DOCSUMO.2023.Available online: https://www.docsumo.com/blog/ocr-accuracy

