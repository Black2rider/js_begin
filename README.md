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
                                     
     
   4. Задача: Крайние элементы массива
Задание
Напиши функцию getExtremeElements(array) которая принимает один параметр array - массив элементов произвольной длины. Функция должна возвращать массив из двух элементов - первого и последнего элемента параметра array.
                                     
           function getExtremeElements(array) {
           // Change code below this line
           const elements = [];
           elements[0] = array[0];
           elements[1] = array[array.length - 1];
           return elements;
           // Change code above this line
           }                              
                           
  5.  Задача: гравировка украшений
Задание
Сервису гравировки украшений нужна функция, которая бы автоматически считала цену гравировки, в зависимости от количества слов и цены за слово.

Объявлена функция calculateEngravingPrice(message, pricePerWord). Эта функция принимает строку, состоящую из слов разделённых только пробелами (параметр message) и цену гравировки одного слова (параметр pricePerWord).

Напиши тело функции, чтобы она возвращала общую стоимость гравировки всех слов в строке.
                                      
          function calculateEngravingPrice(message, pricePerWord) {
          // Change code below this line
           let array = message.split(' ');
           let result = array.length * pricePerWord;
          return result;
           // Change code above this line
            }
            console.log(calculateEngravingPrice('украшений нужна функция', 3))                           

                                     
   6. Задача: композиция массивов
Задание
Напиши функцию makeArray(firstArray, secondArray, maxLength) для создания нового массива со всеми элементами двух исходных firstArray и secondArray. Параметр maxLength содержит максимально допустимую длину нового массива.

Если количество элементов нового массива больше maxLength, функция должна вернуть копию массива длиной maxLength элементов. В противном случае функция должна вернуть новый массив целиком.
                                     
         function makeArray(firstArray, secondArray, maxLength) {
         // Change code below this line
         let newArray = firstArray.concat(secondArray);
         let Array;
         if (newArray.length > maxLength) {
          Array = newArray.slice(0, maxLength); 
          } else {
        Array = newArray;
        }
         return Array;
          // Change code above this line
         }
         console.log(makeArray(["Mango", "Poly", "Houston"], ["Ajax", "Chelsea"], 4));       
   
   

   7.  Задача: сумма чисел (цикл for)
Задание
Напиши функцию calculateTotal(number), которая принимает целое число (параметр number) и возвращает сумму всех целых чисел от единицы и до этого числа. Например, если number равно 3, то сумма это 1 + 2 + 3, то есть 6.
   
             function calculateTotal(number) {
             // Change code below this line
              let summ = 0;
             for (let i = 0; i <= number; i += 1) {
                 summ += i;
             }
              return summ;

              // Change code above this line
            } console.log(calculateTotal(3));
  

                                        
     8.  Задача: подсчёт суммы покупки
Задание
Напиши функцию calculateTotalPrice(order), которая принимает один параметр order - массив чисел, и рассчитывает общую сумму его элементов. Общая сумма элементов должна сохраняться в переменной total, которая возвращается, как результат работы функции.
                                        
                                        
                function calculateTotalPrice(order) {
                 let total = 0;
                 // Change code below this line
                 for (let i = 0; i < order.length; i +=1) {
                    total += order[i]; 
                 }
                 // Change code above this line
                 return total;
               }                       

   
   
   9.  Задача: поиск самого длинного слова
Задание
Напиши функцию findLongestWord(string) которая принимает произвольную строку состоящую только из слов разделённых пробелом (параметр string) и возвращает самое длинное слово в этой строке.
   
                function findLongestWord(string) {
                 // Change code below this line
                 let newArray = string.split(' ');
                 let maxWord = newArray[0];
                 for (let i = 0; i < newArray.length; i += 1) {
                     if (newArray[i].length > maxWord.length) {
                        maxWord = newArray[i]; 
                     }
                 }
                  return maxWord;

                 // Change code above this line
               }

   
   
   10.  Задача: фильтрация массива чисел
Задание
Напиши функцию filterArray(numbers, value), которая принимает массив чисел (параметр numbers) и возвращает новый массив, в котором будут только те элементы массива numbers, которые больше чем значение параметра value (число).
   
                  
                    unction filterArray(numbers, value) {
                     // Change code below this line
                    let newArray = [];
                    for (const number of numbers) {
                       if (number > value) {
                         newArray.push(number); 
                       }
                    }
                    return newArray;

                    // Change code above this line
                  }

   
   11.  Задача: общие элементы
Задание
Общими элементами массивов называют те элементы, которые присутствуют во всех массивах.

Например, в двух массивах [1, 3, 5] и [0, 8, 5, 3] общими будут числа 3 и 5, т.к. они присутствуют в обоих исходных массивах. А числа 0, 1 и 8 присутствуют только в одном из массивов.

Напиши функцию getCommonElements(array1, array2) которая получает два массива произвольной длины в параметры array1 и array2, и возвращает новый массив, состоящий из тех элементов, которые присутствуют в обоих исходных массивах.
   
   
                    function getCommonElements(array1, array2) {
                       // Change code below this line
                       let array3 = [];
                       for (const number of array1) {
                         if (array2.includes(number)) {
                            array3.push(number); 
                         }

                       }
                       return array3;

                      // Change code above this line
                     }
