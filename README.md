# Sistema de Monitoramento Sem Fio para Refrigeradores de Vacinas
### Descrição do projeto
<p>
Este projeto propõe uma Rede de Sensores Sem Fio (RSSF/WSN) para o monitoramento das condições de armazenamento de vacinas em refrigeradores. O sistema tem como objetivo acompanhar continuamente a temperatura e o estado da porta, permitindo identificar condições anormais e gerar alertas para auxiliar os profissionais responsáveis pelo armazenamento.
</p>

![image alt](https://github.com/MarioPorco/TP546-IOT/blob/119b16be80166a8b2aa06b872eeb72bc61328e1a/Jeringas.png)

### Problema identificado
<p>
As vacinas necessitam de condições adequadas de armazenamento para manter sua qualidade e eficácia. Quando a temperatura permanece fora dos limites recomendados, especialmente por períodos prolongados, as vacinas podem sofrer alterações e perder sua eficácia. Por isso, é importante realizar o monitoramento constante da temperatura, permitindo identificar rapidamente qualquer alteração e tomar as medidas necessárias antes que ocorram perdas
</p>

![image alt](https://github.com/MarioPorco/TP546-IOT/blob/d884e6718be13c5411d66d1cd585b47e521a7774/Vacunas.png)
### Solução proposta
<p>
Propõe-se o desenvolvimento de um sistema baseado em Internet das Coisas (IoT) e Rede de Sensores Sem Fio (RSSF) para realizar o monitoramento contínuo das condições de armazenamento das vacinas. O sistema será composto por sensores instalados no refrigerador e por um ESP32, responsável por receber e processar as informações obtidas. Essa abordagem permite automatizar a coleta dos dados e reduzir a dependência do monitoramento manual.
</p>

![image alt](https://github.com/MarioPorco/TP546-IOT/blob/b67cb3f4c74f3fc102a8bff1cf83a4057a01fdcc/Diagrama%20de%20bloques_IoT.jpg)
<p>
A partir dos dados processados pelo ESP32, as informações serão transmitidas por meio de comunicação sem fio para um sistema de armazenamento, onde poderão ser registradas e consultadas posteriormente. Dessa forma, será possível acompanhar o histórico das condições do refrigerador e identificar rapidamente possíveis alterações. Caso seja detectada uma condição fora dos limites estabelecidos, o sistema poderá gerar um alerta para o usuário, permitindo uma intervenção mais rápida.
</p>

### Sensores e processamento
<p>
Para o monitoramento da temperatura, propõe-se uma termopar tipo K associada ao MAX31855. Para detectar a abertura da porta, utiliza-se um sensor magnético. O ESP32 recebe essas informações e verifica se os valores estão dentro dos limites estabelecidos.
</p>

![image alt](https://github.com/MarioPorco/TP546-IOT/blob/e898ae22712a54779e9afeb8827b7cdbf90c05e7/ESP32.png)
##### Modulo ESP32

![image alt](https://github.com/MarioPorco/TP546-IOT/blob/e898ae22712a54779e9afeb8827b7cdbf90c05e7/TipoK.png)
##### MAX31855 Termopar Tipo K

![image alt](https://github.com/MarioPorco/TP546-IOT/blob/e898ae22712a54779e9afeb8827b7cdbf90c05e7/Littelfuse.png)
##### Littelfuse FLEX-14

### Armazenamento e alertas
<p>
Os dados coletados pelos sensores serão enviados pelo ESP32 por meio de comunicação sem fio e registrados em um sistema de armazenamento. Dessa forma, será possível manter um histórico das medições, permitindo consultar posteriormente as condições de temperatura e os eventos registrados no refrigerador. Essa arquitetura é semelhante à utilizada em sistemas IoT de monitoramento de vacinas que combinam armazenamento de dados, visualização em tempo real e comunicação sem fio.
</p>

![image alt](https://github.com/MarioPorco/TP546-IOT/blob/3d954d23f3a5e9c13830af62b3e5b6ed745107a8/Almacenamiento%20de%20datos.jpg)

### REFERÊNCIAS BIBLIOGRÁFICAS
<p>
Addendum, M. V. (2024). Vaccine Storage and Handling Toolkit. https://lalinks.org/linksweb/docs/vfc/Vaccine%20Storage%20and%20Handling%20Toolkit%20Mpox%20Vaccine%20Addendum%20-%20March%202024.pdf

De la Cruz Castro, A. F., & Soldevilla Curo, J. C. (2023). Internet de las cosas para mejorar el monitoreo de la cadena de frio en vacunas del Centro de Salud Daniel Hernández. https://doi.org/https://hdl.handle.net/20.500.14597/5773

Furtado, V. G., da Silva, Y. F., & da Fonseca Neto, J. V. (2023). Rede de Sensores Sem Fio e Aprendizado de Máquina para Monitoramento da Qualidade de Ambientes de Estudo. 1(2). https://doi.org/https://doi.org/10.20906/SBAI-SBSE-2023/3837

GONTIJO, T. L. (2021). Avaliação da cadeia de frio do transporte de vacina: estudo transversal em Minas Gerais, Brasil. Revista de APS. https://doi.org/10.34019/1809-8363.2019.v22.16032 

Jiang, S., Jia, S., & Guo, H. (2024). Internet of Things (IoT)-enabled framework for a sustainable Vaccine cold chain management system. Heliyon, 10(7). https://doi.org/10.1016/j.heliyon.2024.e28910

Patine, F. dos S., Lourenção, L. G., Wysocki, A. D., Santos, M. de L. S. G., Rodrigues, I. C., & Vendramini, S. H. F. (2021). Análise da perda de vacinas por alteração de temperatura. Revista Brasileira de Enfermagem, 74, e20190762. https://doi.org/https://doi.org/10.1590/0034-7167-2019-0762

Pesantes Castro, N. A., & Rodríguez Zúñiga, C. D. (2024). Diseño e implementación de un prototipo para el control y monitoreo mediante IoT de la cadena de frío en la transportación de medicamentos. https://dspace.ups.edu.ec/handle/123456789/29091

SILVA, D. J. M. D., OLIVEIRA, F. G. D., NUNES, G. S., PATRIOTA, I. E. P., SANTANA, I. S., SANTOS, J. V. D. C., & SILVA, M. R. G. D. (s.d.). Sistema de refrigeração e monitoramento de vacinas. Recuperado https://ric.cps.sp.gov.br/handle/123456789/43186

Taís de Almeida Gonçalves, D., da Fonseca Viegas, S. M., Siqueira Rennó, H. M., Junqueira Oliveira, V., de Azevedo Guimarães, E. A., Carvalho, H. R. de J., Montenegro, L. C., & Conceição de Oliveira, V. (2021). Conservação de vacinas: O olhar da equipe de enfermagem. Avances en Enfermería, 39, 178–187. https://doi.org/https://doi.org/10.15446/av.enferm.v39n2.86299
</p>
