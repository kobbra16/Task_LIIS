__Scripts postman__

__Метод GET posts__
1.Получаем JSON-ответ и первый объект из массива
```
var jsonData = pm.response.json();
var post = jsonData[0];
```

2.Проверка, что статус ответа 200
```
pm.test("Статус ответа 200", function () {
    pm.response.to.have.status(200);
});
```

3.Проверка, что ответ — массив с одним 
```
pm.test("Ответ является массивом с одним объектом", function () {
    pm.expect(jsonData).to.be.an('array').that.has.lengthOf(1);
});
```
4.Проверка наличия поля id
```
pm.test("Поле 'id' присутствует", function () {
    pm.expect(post).to.have.property('id');
});
```
5.Проверка наличия поля author
```
pm.test("Поле 'author' присутствует", function () {
    pm.expect(post).to.have.property('author');
});
```
6.Проверка наличия поля title
```
pm.test("Поле 'title' присутствует", function () {
    pm.expect(post).to.have.property('title');
});
```
7.Проверка наличия поля publication_datetime
```
pm.test("Поле 'publication_datetime' присутствует", function () {
    pm.expect(post).to.have.property('publication_datetime');
});
```
8. Проверка наличия поля content
```
pm.test("Поле 'content' присутствует", function () {
    pm.expect(post).to.have.property('content');
});
```
__Mетод POST posts__
1.Получаем JSON-ответ
```
var post = pm.response.json();
```
2.Проверка, что статус ответа 200
```
pm.test("Статус ответа 200", function () {
    pm.response.to.have.status(201);
});
```
3.Проверка, что ответ — объект
```
pm.test("Ответ является объектом", function () {
    pm.expect(post).to.be.an('object');
});
```
4.Проверка наличия поля id
```
pm.test("Поле 'id' присутствует", function () {
    pm.expect(post).to.have.property('id');
});
```
5.Проверка наличия поля author
```
pm.test("Поле 'author' присутствует", function () {
    pm.expect(post).to.have.property('author');
});
```
6.Проверка наличия поля title
```
pm.test("Поле 'title' присутствует", function () {
    pm.expect(post).to.have.property('title');
});
```
7.Проверка наличия поля publication_datetime

```
pm.test("Поле 'publication_datetime' присутствует", function () {
    pm.expect(post).to.have.property('publication_datetime');
});
```
// Проверка наличия поля content
```
pm.test("Поле 'content' присутствует", function () {
    pm.expect(post).to.have.property('content');
});
```
Метод Get post
// Получаем JSON-ответ
```
var post = pm.response.json();
```
// Проверка, что статус ответа 200
```
pm.test("Статус ответа 200", function () {
    pm.response.to.have.status(200);
});
```
// Проверка, что ответ — объект
```
pm.test("Ответ является объектом", function () {
    pm.expect(post).to.be.an('object');
});
```
// Проверка наличия поля author
```
pm.test("Поле 'author' присутствует", function () {
    pm.expect(post).to.have.property('author');
});
```
// Проверка наличия поля content
```
pm.test("Поле 'content' присутствует", function () {
    pm.expect(post).to.have.property('content');
});
```
// Проверка наличия поля id
```
pm.test("Поле 'id' присутствует", function () {
    pm.expect(post).to.have.property('id');
});
```
// Проверка наличия поля publication_datetime'
```
pm.test("Поле 'publication_datetime' присутствует", function () {
    pm.expect(post).to.have.property('publication_datetime');
});
```
// Проверка наличия поля title
```
pm.test("Поле 'title' присутствует", function () {
    pm.expect(post).to.have.property('title');
});
```

2.Обнаруженные баги 

>В V2 версии отсутствует поле title,в методах GET posts,POST post,GET post.
B V2 версии отсутствует поле content,в методах GET comment,POST comment,GET comments.
В V2 версии статсус код 500 в методе POST sing in
B V2 версии статус код 403 в методе POST grand user admin role


3.Различие в версиях V1 и V2

>В V2 версии добавились методы GET post pagination,GET comments pagination,PUT grand user admin role.


