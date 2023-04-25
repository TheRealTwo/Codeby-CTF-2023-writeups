# Приключения с флагом: Write-up #
Попадая на сайт, видим лишь гифку. А вот исходный код сайта содержит строку поинтереснее: `<-- part1: CODEBY{y0u -->`

С html всё, теперь лезем в Javascript (main.js).<br/>
Видим интересный комментарий: `// 👇️ Change text color part2: _f0und_ on mouseout`

На очереди CSS (styles.css): `/* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, part3: th3m_,  Safari 7+ */    `

Осталась одна часть флага, но все документы нами уже были просмотрены. Хинт наводит на мысль про файл robots.txt, так что смотрим его:

    User-agent: *
    Disallow: /

    # part4: 4ll}
  
У нас есть все 4 части флага, поэтому соединяем их в один флаг:
    
    CODEBY{y0u_f0und_th3m_4ll}

Как вам таск?
