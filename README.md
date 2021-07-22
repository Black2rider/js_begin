   1.  Задача: доставка товара
Задание
Функция getShippingCost(country) должна проверять возможность доставки товара в страну пользователя (параметр country) и возвращать сообщение о результате хранящееся в переменной message. Обязательно используй инструкцию switch.

Формат возвращаемой строки "Shipping to <country> will cost <price> credits", где вместо <country> и <price> необходимо подставить соотвествующие значения.

Список стран и стоимость доставки:

China - 100 кредитов
Chile - 250 кредитов
Australia - 170 кредитов
Jamaica - 120 кредитов
Из списка видно, что доставка есть не везде. Если указанной страны нет в списке, то функция должна вернуть строку "Sorry, there is no delivery to your country"
  
  function getShippingCost(country) {
  let message;
  // Change code below this line
  switch (country) {
    case 'China':
    message = `Shipping to ${country} will cost 100 credits`;
    break
      
    case 'Chile':
    message = `Shipping to ${country} will cost 250 credits`;
    break
      
    case 'Australia':
    message = `Shipping to ${country} will cost 170 credits`;
    break
      
    case 'Jamaica':
    message = `Shipping to ${country} will cost 120 credits`;
    break
      
    default:
    message = 'Sorry, there is no delivery to your country'
  }
  // Change code above this line
  return message;
}
    
    2.  Задача: форматирование сообщения
Задание
Функция formatMessage(message, maxLength) принимает строку (параметр message) и форматирует её, если длина превышает значение в параметре maxLength.

Дополни код функции так, что если длина строки:

не превышает maxLength, функция возвращает её в исходном виде.
больше maxLength, то функция обрезает строку до maxLength символов и добавляет в конец троеточие "...", после чего возвращает укороченную версию.
    
    function formatMessage(message, maxLength) {
  let result;
  // Change code below this line
  if (message.length <= maxLength) {
     result = message; 
  } else {
     result = message.slice(0, maxLength) + '...';
  }
  /// Change code above this line
  return result;
}
//console.log(formatMessage('message', 9));

                                 
   3.  Задача: проверка спама
Задание
Функция checkForSpam(message) принимает строку (параметр message), проверяет её на содержание запрещенных слов spam и sale, и возвращает результат проверки. Слова в строке параметра message могут быть в произвольном регистре, например SPAM или sAlE.

Если нашли запрещенное слово (spam или sale) то функция возвращает буль true.
Если в строке нет запрещенных слов, функция возвращает буль false.
                                 
      function checkForSpam(message) {
  let result;
  // Change code below this line
  let string = message.toLowerCase();
  if (string.includes('spam')) {
     result = true;
  } else if (string.includes('sale')) {
     result = true; 
  } else {
     result = false; 
  }
  // Change code above this line
  return result;
}
                           
