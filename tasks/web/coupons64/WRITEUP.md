# Купоны64: Write-up #
Нас встречает весьма простенький сайт, на котором проверяются купоны. В пример приведены 3 купона, со скидкой в 10, 13 и 37 процентов.
Под заголовком сказано, что купоны зашифрованы в `base64`, что делает задачу легчайшей, т.к. для расшифровки ничего дополнительного не требуется. Можно использовать онлайн де/инкодеры, но я предпочитаю ручками, в терминале.

Берем на пробу первый купон и расшифровываем его:

    $ echo "QkVTVF9NQVJLRVQxMA==" | base64 -d             
    BEST_MARKET10

Напомню, это был купон на скидку в 10%. Думаю, не сложно догадаться, что зашифровать мы должны `BEST_MARKET100`:

    $ echo "BEST_MARKET100" | base64         
    QkVTVF9NQVJLRVQxMDAK

Вставляем получившийся купон на проверку:

    Valid coupon for CODEBY{wh4t_m34ns_s1xty_f0ur} discount for truly l33t dev!

Как по мне, слишком уж простые 350 баллов для среднего таска, не правда ли?