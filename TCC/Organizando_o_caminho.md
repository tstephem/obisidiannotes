Primeiramente aprendi sobre detecção de imagens com redes neurais e sobre o yolo, dai decidimos fazer um trabalho de detecção usando yolov5 no dataset trash_ICRA19. Dataset esse que foi usado num estudo por Fulton em 20xx, comparando modelagens da época dentre elas yolov2.

Primeiramente aplicamos a modelagem do yolov5 no dataset para ver como ele se comportou com os avanços do yolo. O modelo foi treinado com as imagens em 960px por 100 epochs e depois validadas em diferentes tamanhos do mesmo set de validação. Obtemos assim os seguintes resultados:

| MAP  50   | 480px  | 640px  | 960px |
| ------- | ------ | ------ | ----- |
| Plastic | 0,858  | 0,841  | 0,81  |
| Bio     | 0,0155 | 0,0195 | 0,056 |
| ROV     | 0,328  | 0,526  | 0,508 |
| All     | 0,401  | 0,462  | 0,458 |

Com isso observamos que a detecção foi boa para platicos nos 3 tamanhos mas num geral teve uma má performance ficando com MAP geral abaixo de 50%, com isso fez-se interessante buscar formas de contornar a situação. A primeira ideia foi checar a matriz de confusão e ver como a validação está se comportando:

![[confusion_matrix_t.png]]

Num olhar geral, na validação de 960px ,podemos ver que realmente quando temos plastico o modelo tem detectado em 66% dos casos e marcado no nada em 29% dos casos. Quanto as imagens que temos bio marcada o modelo previu que era fundo de imagem em 77% dos casos. O ROV o modelo tem cnfundido um pouco com o fundo das imagens tbm. E de marcações erradas temos que 68% das vezes foi em plastico. Com isso surgiram dois caminhos:

- Refazer as marcações do dataset trash_ICRA19 para deixar mais acurado as marcações que temos [Aqui](obsidian://open?vault=Meus_Cadernos&file=TCC%2FNewBoundingBoxes%2FRemarcar%20os%20dataset%20trash_ICRA19) 
- Adicionar mais imagens de outros datasets com intuito de preencher o espaço mal distribuido de marcações