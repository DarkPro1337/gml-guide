---
title: "Условия – оператор switch"
date: 2019-08-02T22:14:06+03:00
draft: false
weight: 40
pre: <b>6. </b>
---
Возможно, как новичку, операторы **switch**, не будут очень полезны для вас, но все же вы должны знать о них.

В операторе **switch** вы сначала указываете переменную, функцию или комбинацию внутри математическом выражении. Затем вы перечисляете все возможные случаи. Оператор **switch** вычисляет указанное выражение и переходит к случаю, соответствующему результату. Он выполняет код, следующий за случаем, пока не будет найден разрыв.

 Вот пример:

```gml
switch(level){
  case 1: level_name = "Overworld"; break;
  case 2: level_name = "Underground"; break;
  case 3: level_name = "Water World"; break;
  case 4: level_name = "Castle"; break;
  default: level_name = "Unknown";
}
```

В этом примере `level` - это переменная, которая содержит номер уровня, на котором игрок находится в данный момент. Когда `level` равен 1, он переключится в `case 1`. Он будет запускать код, где он устанавливает `level_name` для «Overworld». Затем он сталкивается с `break` и останавливает код.

{{% notice note %}}
Если вы не используете `break` перед запуском другого случая, он будет продолжать выполнять все случаи до тех пор, пока не будет найден разрыв.
{{% /notice %}}

Аналогично, когда `level` равен 2, будет выполняться случай 2. То же самое для случаев 3 и 4.

Но что, если `level` не соответствует ни одному из этих случаев? В такой ситуации **switch** перейдет к части `default` и запустит код идущий после него.
