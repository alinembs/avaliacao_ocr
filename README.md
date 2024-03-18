# Avaliacao OCR 
Repositório da Task para Avaliar ferramentas de Extração de Texto
 #### Ferramentas Usadas
  
| Ferramenta | Abordagem | 
|    :---:   |     :---:     |  
|  Pytesseract|   OCR |   
|  PDFX|   TS   |    
| PyMuPDF| TS |
| PyPdf2| TS |

 #### Documentos Usados para o teste

| Dataset|   Documento |    Link      | Nº de Paginas |
| :---:  |    :---:    |     :---:    |  :---:        |
|Dataset 1 |  Notes on the Paranormal by Ben Steigmann| https://encurtador.com.br/fgLPX |  185 |
|Dataset 2 |  Diálogo entre a sociologia e a psicanálise: o indivíduo e o sujeito by SciELO - EDUFBA | https://encurtador.com.br/cmPU2  | 287|
|Dataset 3| Iracema (Versão original) by José de Alencar     |   https://encurtador.com.br/bdgmD  |  143 |   
|Dataset 4|  O Paraíso Perdido, John Milton ( Ediouro) - John Milton's Paradise Lost: A Literal translation for portuguese in prose text by Ediouro, John Milton, Conceição G. Sotto Maior  | https://encurtador.com.br/cdz45    |   261 |
| Dataset 5| Histórias e Tradições da Cidade de Sao Paulo by Ernani Silva Bruno     |  https://encurtador.com.br/hkoGW   |  686|
       

 #### Resultados do Tempo
  
| Ferramenta | Tempo  em segundos| 
|    :---:   |  :---:    |  
|   Pytesseract |     4085,82     | 
|   PDFX    |       49,07    |  
|   PyMuPDF   |      2,58    |    
|   PyPdf2  |       76,38   |  




 #### Taxa de Erro de Caractere (CER)
  
| Ferramenta  | Dataset 1 |Dataset 2 |Dataset 3 |Dataset 4 |Dataset 5 |Desvio Padrão |
|    :---:    |  :---:    |   :---:   | :---:    | :---:    | :---:    | :---:       | 
| Pytesseract | 2,15%     |  5,43%    |  5,13%   | 11,29%   |  27,55%  |             |
| PDFX        | 8,41%     | 9,13%     | 11,97%   | 3,96%    | 3,76%    |             |
| PyMuPDF     |  1,97%    |  2,11%    | 5,06%    |  4,07%   | 0,8%     |             |
| PyPdf2      | 2,05%     |  5,91%    | 4,86%    | 11,52%   | 1,97%    |              |
 #### Taxa de Erro de Palavras (WER)
  
| Ferramenta  | Dataset 1 |Dataset 2 |Dataset 3 |Dataset 4 |Dataset 5 |Desvio Padrão |
|    :---:    |  :---:    |   :---:   | :---:    | :---:   | :---:    | :---:        | 
| Pytesseract | 18,14%    | 32,03%    |27,74%    | 36,32%  | 46,24%   |              |
| PDFX        | 6,67%     | 11%       |18,42%    | 7,38%   | 3,82%    |              |
| PyMuPDF     |8,12%      | 8,94%     | 25,90%   | 9,79%   | 0,34%    |              |
| PyPdf2      | 8,14%     | 11,51%    |  25,95%  | 9,90%   | 0,33%    |              |
