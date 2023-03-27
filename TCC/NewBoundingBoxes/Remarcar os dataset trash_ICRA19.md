O Dataset inicial tinha poucas marcações e deixava de fora algumas marcações que podiam ser mais acuradas. Com isso, decidi usar a ferramenta do site [Roboflow](https://roboflow.com). Segue alguns exemplos das alterações realizadas:
![[obj0309.png]]
![[obj0309a.png]]
![[obj0707.png]]
![[obj0707a.png]]
![[obj1314.png]]
![[obj1314a.png]]

Após isso refiz o treinamento e validei tanto nas imagens de validação sem as novas marcações e com as novas marcações.

- Nas imagens de validação com marcações antigas (yolo s)
| MAP 50  | 480px  | 640px  | 960px  |
| ------- | ------ | ------ | ------ |
| Plastic | 0,84   | 0,866  | 0,816  |
| Bio     | 0,0384 | 0,0275 | 0,0349 |
| ROV     | 0,407  | 0,38   | 0,446  |
| All     | 0,429  | 0,424  | 0,432  |

- Nas imagens com as marcações novas (yolo s)
| MAP  50   | 480px  | 640px  | 960px |
| ------- | ------ | ------ | ----- |
| Plastic | 0,767  | 0,796  | 0,761  |
| Bio     | 0,294 | 0,312 | 0,3 |
| ROV     | 0,45  | 0,437  | 0,519 |
| All     | 0,504  | 0,515  | 0,527 |

Alguns resultados mais aprofundados [Aqui](obsidian://open?vault=Meus_Cadernos&file=TCC%2FNewBoundingBoxes%2FValida%C3%A7%C3%A3o%20Trash_ICRA19v3) 

