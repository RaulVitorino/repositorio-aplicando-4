🚀 Controle e gestão do consumo de água das residências	: usando a IoT para economizar e gerir os recursos hídricos 


Status ✨

O projeto está funcional para a aplicação no qual foi pensado, no entanto, a parte do sensor de fluxo precisa ser aprimorada na parte elétrica a fim de reduzir o ruído de sinal e trazer mais precisão e exatidão a suas medições.


Linguagens 🚀

Esse projeto foi escrito em linguagem C++. Também usa o JavaScript para trabalhar com dados, no caso, usando o JSON.


Resumo do projeto 📌

o sensor de nível está na parte interna do reservatório de água, na parte superior do reservatório. À medida que a água do reservatório diminui devido ao uso, o sensor de fluxo 
detecta a passagem da água e e emite pulsos para o esp 32, contabilizando o volume de água que passo e foi consumido. Quando a água do reservatório baixa o nível, 
o sensor de nível do reservatório é ativado e o esp 32 envia uma mensagem via mqtt para o esp 01, que por sua vez, liga a bomba d’água por meio de um rele, 
enchendo o reservatório até a medida que a água atinge a altura do sensor de nível do reservatório, indicando que já encheu de água, então o esp 32 envia uma mensagem para o esp 01 que
resulta no corte da correte elétrica da bomba d’água por meio do rele. A comunicação entre os dois esp aconteceu via mqtt hivemq e a visualização das mensagens enviadas foi feita pelo
software MQTT Explorer. A visualização das mensagens pelo MQTT Explorer se deu por meio da identificação, na árvore de tópicos, do tópico "nivel" e a partir de então, as mensagens 
enviadas eram visualizadas quase que instantaneamente, com um pequeno delay.

No esp 32 foram utilizados os pinos 14 e 27 para os sensores de nível e fluxo, respectivamente. No esp 01 foi utilizado o pino 2 para controlar o relê.

Pelo relê passava uma corrente de 12V que servia de alimentação para o motor. O esp 01 foi alimentado por uma corrente de 5V, bem como o esp 32.

Segue o link do projeto: https://github.com/RaulVitorino/repositorio-aplicando-4/blob/main/Artigo%20projeto%20de%20IoT%20final.pdf

Segue o link da apresentação do projeto: https://youtu.be/g6DmTQKFGOM?si=C8ZYR7MEs-rRZCmN

Segue o link para a demonstração do mqtt: https://www.youtube.com/watch?v=wt46ds-iPzk


📚 Componentes utilizados

![image](https://github.com/user-attachments/assets/20544484-be6c-4f9c-8a9e-cdad5e76b5cc)
Esp 32

![image](https://github.com/user-attachments/assets/b615b71d-ca9f-4e1f-818c-cc49ceb243a6)
Esp 01

![image](https://github.com/user-attachments/assets/5e302021-e74f-47bc-b60c-e797186c8780)
Sensor de nível

![image](https://github.com/user-attachments/assets/c7adc724-d468-475a-add6-2c6bf2ecba78)
Sensor de fluxo

![image](https://github.com/user-attachments/assets/77e9ee09-bdc4-413d-a188-af9d9352dc09)
Mini bomba d'água

Contribuição 🤝
Este é um projeto de código aberto para qualquer pessoa poder aprender, sugerir melhorias e fazer aplicações!

Se você encontrar problemas ou tiver sugestões, vamos discuti-las.

