# Avaliação de algorítmos para determinação de rotas mais curtas para pontos de coleta de ovitraps

## Autor:  
### Maurício Matheus Araújo Silva Galvão - Engenharia de Computação (DCA/UFRN)   

Link do vídeo explicativo: https://drive.google.com/drive/u/0/folders/1grbua5v5ulgaxSdwFQZqX33Of9oLDP1y


Nesta atividade foi avaliado o desempenho de 10 colaboradores ao saírem do ponto de origem, que é o Centro de Controle de Zoonoses, Natal, para 65 pontos de coletas de ovitraps em função ao combate à dengue. Foram utilizados 3 algorítmos para avaliação:  

• Dijkstra padrão;  

• Dijkstra com heap; 

• OSMNx.  

O código foi feito em Python com a utilização das seguintes bibliotecas: `OSMNx`, `Codecarbon`, `Matplotlib.pyplot`, `Networkx`, `Pandas`, `Ortools.constrait_solver`, `Geopy.distance` e `Numpy`.   

Primeiramente criamos um grafo da cidade de Natal/RN, assim obtendo as coordenadas do ponto de origem, que foi o Centro de Controle de Zoonoses e posteriormente dos 65 pontos de coleta referenciados como destinos, organizados em um arquivo .csv contendo suas devidas coordenadas. Com isso pudemos aplicar os três algorítmos separadamente analisando as suas pegadas de carbono com ajuda da biblioteca `Codecarbon`, o que nos deu uma visão bem detalhada dos custos energéticos e ambientais da execução de cada um deles. Após esse processo, conseguimos visualizar quais foram as rotas mais curtas encontradas para coleta dos colaboradores.

## Pontos de coleta de ovitraps:    

![image](https://github.com/user-attachments/assets/bdb334e5-5881-41df-bddd-da5d8beff6a6)   


## Melhor caminho encontrado (Dijkstra com Heap):     

• Rota Colaborador 1: 7 casas. Distância: 54.21 km  
• Rota Colaborador 2: 12 casas. Distância: 54.68 km  
• Rota Colaborador 3: 6 casas. Distância: 54.60 km  
• Rota Colaborador 4: 8 casas. Distância: 54.72 km  
• Rota Colaborador 5: 13 casas. Distância: 51.98 km  
• Rota Colaborador 6: 3 casas. Distância: 34.27 km  
• Rota Colaborador 7: 5 casas. Distância: 54.61 km  
• Rota Colaborador 8: 7 casas. Distância: 35.64 km  
• Rota Colaborador 9: 3 casas. Distância: 38.30 km  
• Rota Colaborador 10: 1 casas. Distância: 35.54 km  

**Distância total combinada para todos os colaboradores: 468.54 km**

![image](https://github.com/user-attachments/assets/4ae0f976-4f56-46fe-a176-b5c381070b68)


## Melhor caminho encontrado (A*):     

• Rota Colaborador 1: 7 casas. Distância: 54.21 km  
• Rota Colaborador 2: 12 casas. Distância: 54.68 km  
• Rota Colaborador 3: 6 casas. Distância: 54.60 km  
• Rota Colaborador 4: 8 casas. Distância: 54.72 km  
• Rota Colaborador 5: 13 casas. Distância: 51.98 km  
• Rota Colaborador 6: 3 casas. Distância: 34.27 km  
• Rota Colaborador 7: 5 casas. Distância: 54.61 km  
• Rota Colaborador 8: 7 casas. Distância: 35.64 km  
• Rota Colaborador 9: 3 casas. Distância: 38.30 km  
• Rota Colaborador 10: 1 casas. Distância: 35.54 km  

**Distância total combinada para todos os colaboradores: 468.54 km**

![image](https://github.com/user-attachments/assets/8b68e41a-ad21-462b-870a-634d9408b539)  

## Tabela de comparação entre os algorítmos:  

![image](https://github.com/user-attachments/assets/898a21b2-5a47-4883-81ce-84f55907fdc4)  

Analisando os mapas resultantes, podemos perceber que ambos os algorítmos Dijkstra e A* escolheram a mesma opção de rotas mínimas, isso devido ao fato de que apesar de terem métodos e velocidades diferentes, todos eles são projetados para encontrar a mesma e única resposta correta: o caminho mais curto entre dois pontos. Em consequência a isso, o OR-Tools recebeu a mesma planilha de custo todas as vezes, criando o mesmo plano de rotas otimizado.  

A demora de execução, consumo elevado de energia e alta quantidade de Co2 do Dijkstra padrão é explicada pela complexidade do algorítmo (O(n²)), o que significa uma certa ineficiência do método de busca dentro de um problema de grande escala, como o mapa de uma cidade, o que não acontece com o A* e nem com o Dijkstra que utiliza heap por serem bem mais otimizados.  





