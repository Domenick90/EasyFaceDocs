                                          Дополнительне функции EasyFace для новых часов

# LineProgress
![image](https://github.com/Domenick90/EasyFaceDocs/assets/57414291/05de774a-6a60-43c7-b077-5e06a55a070a)
![image](https://github.com/Domenick90/EasyFaceDocs/assets/57414291/c2b69ed0-b7dd-4f16-b507-cb3455393c95)
вот так координаты выставляются:
берете компонент **CircleProgress** и даете ему имя **lineProgress_<название>**
_Center X/Y_ — начальная координата, 
_AngleStart/End_ — конечная. 
Радиуса там нет, разумеется, есть толщина линии и закругленные/плоские концы

# Circle Progress. Работающие настройки
![image](https://github.com/Domenick90/EasyFaceDocs/assets/57414291/eb6e0894-e014-4b90-98be-82a259af618a)

# Поддержка JS-Application
Даём виджету(Image) имя btn_[имя_скрипта_из_app.js] и выбираем нужную прозрачную картинку.
![image](https://github.com/Domenick90/EasyFaceDocs/assets/57414291/98c04ed2-060d-44d3-9997-8c9939189de7)

# Поддержка Tap Buttons
Даём виджету(Image) имя btn_[название_действия_из_списка]_RGBA и прикрепляем прозрачную картинку

![image](https://github.com/Domenick90/EasyFaceDocs/assets/57414291/9edddd4b-f035-4ae6-97a7-d066aab44897)
![image](https://github.com/Domenick90/EasyFaceDocs/assets/57414291/50881d86-beaf-499d-84b9-bea52d017a01)

# Добавление альфа-канала (прозрачности) для виджета типа Image с RLE-сжатием
Дописываем в имя виджета *_RGBA
# Примеры ID и картинок погоды для RW-2, RW-3, MB7Pro (нужно оставить только 40 индексов иначе не переварит), MB8
![image](https://github.com/Domenick90/EasyFaceDocs/assets/57414291/64fe76c9-3298-416b-a89a-358855348f77)

                                          Пример для Gen2:
![image](https://github.com/Domenick90/EasyFaceDocs/assets/57414291/06da0f7e-2a88-49fb-bbec-a677b70974e7)

[Погода RW2 10 картинок 45 индексов.zip](https://github.com/Domenick90/EasyFaceDocs/files/11494183/RW2.10.45.zip)

# Примеры картинок для вывода дистанции на циферблат в км.
[distance_images.zip](https://github.com/Domenick90/EasyFaceDocs/files/11494192/distance_images.zip)

## FAQ по циферблатам для Gen2
1. Компилятор не знает подпапки, изображения необходимо располагать в корневой папке images
2. Разрешение изображений для каждого набора должно быть одинаковым
3. Дни недели и погода делаются только через через imageList (если месяцы в текстовом формате, то также). Дни недели с воскресенья - 0 index, месяца с января - 1 index
4. Для иконок погоды лучше распаковать проверенный циферблат и посмотреть на соответствие индексов изображениям
5. Для создания AOD необходимо в основной папке с проектом создать папку AOD и скопировать туда папки Images и fprj основного циферблата. После подгонки AOD'а (передвинуть/удалить лишние элементы и тд) просто сохранить этот проект в EasyFace без компиляции
6. Для первичной проверки на ошибки можно пользоваться распаковщиком (см. закреп)
7. Превью можно получить распаковав циферблат
8. Разрешение циферблата 466*466, а превью 246*246
9. Значение Negative sign заполнять обязательно, можно установить любую цифру из набора, как правило выбирают "0". Для значений температуры там устанавливают знак "-"
10. Если в аналоговом циферблате какие-то стрелки не нужны (например секунды), то не нужно их делать
11. Если на циферблате черный фон, то картинку фона делать не нужно. Отсутствие фона часы трактуют как черное
12. Прозрачные картинки объем циферблата не уменьшают. Объем снижает уменьшение линейных размеров изображений. В общем, чем меньше размеры картинок, тем лучше.
13. Использование одних и тех же изображений существенно снижает объемы циферблатов. Поэтому лучше не использовать много разных элементов, а стараться минимизировать количество разных шрифтов, цветов и т.п. оформительских элементов.
Это и в плане дизайна лучше, чем "многоцветье форм и размеров"




> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
