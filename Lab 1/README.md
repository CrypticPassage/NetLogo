## Комп'ютерні системи імітаційного моделювання
## СПм-22-3, **Ніколаєнко Дмитро Сергійович**
### Лабораторна робота №**1**. Опис імітаційних моделей та проведення обчислювальних експериментів

<br>

### Варіант 2, модель у середовищі NetLogo:
[Climate Change](https://www.netlogoweb.org/launch#http://www.netlogoweb.org/assets/modelslib/Sample%20Models/Earth%20Science/Climate%20Change.nlogo)

<br>

### Вербальний опис моделі:
Модель "Climate Change" досліджує вплив різних факторів на температуру Землі, зосереджуючись на таких аспектах, як альбедо земної поверхні, хмарність, кількість вуглекислого газу в атмосфері, інтенсивність сонячного світла. Модель показує залежність глобальної температури відносно заданих параметрів. 

### Керуючі параметри:
- **sun-brightness** визначає частоту падіння сонячних променів.
- **albedo** визначає ступінь відбиття земною поверхнею сонячних променів. Чим більший показник альбедо, тим більше променів відбивається поверхнею.
- **clouds** визначає кількість хмар у небі. Хмари здатні відбивати сонячні промені.
- **CO2** визначає кількість молекул CO2 у повітрі. Молекули CO2 відбивають тепло, яке виходить з земної поверхні.

### Внутрішні параметри:
- **sky-top**. Верхня точка неба. Обмежує площу появи хмар та молекул СO2.
- **earth-top**. Верхня точка земної поверхні.
- **temperature**. Показник температури земної поверхні.

### Показники роботи системи:
- Залежність температури від часу. Графік, який показує, як змінюється температура земної поверхні з плином часу відносно наших заданих параметрів.

### Примітки:
При налаштуваннях краще не обирати занадно великі показники кількості хмар та/або вуглекислого газу. Це сприяє великому навантаженню на моделюванная та може спричинити неможливість контролювати імітацію.

### Недоліки моделі:
Основним недоліком моделі можна назвати її обмеженість. В моделі не змінюється угол нахилу сонячних променів відносно часу, неможливо додати або видалити конкретну кількість хмар або молекул CO2, вони задаються рандомним або статичним значенням. Неможливо задати стартове значення температури земної поверхні, змінити швидкість руху об'єктів. Модель не враховує багато факторів, які можуть впливати на результати симуляції, такі як, дощ, пора року.

## Обчислювальні експерименти
### 1. Вплив показнику sun-brightness на температуру земної поверхні
Досліджується, як змінюється температура земної поверхні відносно параметру sun-brigthtness. Інші параметри залишаються за замовчуванням.

<table>
<thead>
<tr><th>показник sun-brightness</th><th>показник температури земної поверхні на 500-му такті</th></tr>
</thead>
<tbody>
<tr><td>0.5</td><td>13</td></tr>
<tr><td>1</td><td>15.1</td></tr>
<tr><td>1.5</td><td>16.2</td></tr>
<tr><td>2</td><td>17</td></tr>
<tr><td>2.5</td><td>18.7</td></tr>
<tr><td>3</td><td>19.3</td></tr>
</tbody>
</table>

![!\[Alt text\](image.png)](<Sunbright.png>)

На основі наведеної таблиці можна зробити висновок, що збільшення показнику sun-brightness сприяє збільшенню температури земної поверхні.

### 2. Вплив показнику clouds на температуру земної поверхні
Досліджується, як змінюється температура земної поверхні відносно параметру clouds. Інші параметри залишаються за замовчуванням.

<table>
<thead>
<tr><th>показник clouds</th><th>показник температури земної поверхні на 500-му такті</th></tr>
</thead>
<tbody>
<tr><td>1</td><td>13.1</td></tr>
<tr><td>3</td><td>13.4</td></tr>
<tr><td>5</td><td>13.8</td></tr>
<tr><td>7</td><td>12.6</td></tr>
<tr><td>9</td><td>12.3</td></tr>
<tr><td>11</td><td>12.1</td></tr>
</tbody>
</table>

![!\[Alt text\](image.png)](<Clouds.png>)

На основі наведеної таблиці можна зробити висновок, що збільшення показнику clouds загалом сприяє зменшенню температури земної поверхні. Хмари выдбивають сонячне світло, не даючи йому добратися до земної поверхні. Проте, згідно таблиці, можна побачити що збільшення хмар не завжди зменшує температуру загалом. Це зв'язано з тим, що ми не можемо регулювати в моделі розмір хмари та її положення, швидкість переміщення. Проте, можно впевнено сказати, що значна кількість хмар на небі призведе до зменшення температури.

### 3. Вплив показнику CO2 на температуру земної поверхні
Досліджується, як змінюється температура земної поверхні відносно параметру CO2. Інші параметри залишаються за замовчуванням.

<table>
<thead>
<tr><th>показник CO2</th><th>показник температури земної поверхні на 10000-му такті</th></tr>
</thead>
<tbody>
<tr><td>25</td><td>27.8</td></tr>
<tr><td>50</td><td>29.2</td></tr>
<tr><td>75</td><td>33.4</td></tr>
<tr><td>100</td><td>33.2</td></tr>
<tr><td>125</td><td>34.9</td></tr>
<tr><td>150</td><td>39.9</td></tr>
</tbody>
</table>

![!\[Alt text\](image.png)](<Gas.png>)

На основі наведеної таблиці можна зробити висновок, що збільшення показнику CO2 сприяє збереженню температури земної поверхні. Вуглекислий газ відбиває теплове випромінювання поверхні назад, тим самим зберігаючи тепло. Проте, згідно таблиці, можна побачити, що незначне збільшення кількості вуглекислого газу не завжди зберігає температуру краще, ніж коли вуглекислого газу менше. Це зв'язано з тим, що ми не можемо регулювати інтенсивність вуглекислого газу в просторі, тому коли його мало, то воно може не відбити віпромінювання назад швидкість. Проте, можно впевнено сказати, що значна кількість вуглекислого газу в небі призведе до значного збереження температури. 
