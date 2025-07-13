![my photo](/my_photo.png)

# Nadtochaev Aleksandr CV
___
civil engineer

___

## Contact information:

**Phone number**: + 375 29 399-04-20

**E-mail**: Nadtochaev_aleksandr@mail.ru

**Telegram**: @Aleksandr_Nadtochaev

**Linkedn**: [александр-надточаев](www.linkedin.com/in/александр-надточаев-78ab118b)

___

## About me:
I am a civil engineer. I graduated from Belarusian state university of transport in 2014. Since then until today my work has been related to construction. I worked in different part of constraction - on construction site, engineer in constractor's service, customer service engineer. I like this job but it is dificult and not well paid job. I had reached a limit beyond which is very difficult to develop. I decided to try something else.

IT sphere is always interested me. I think it is very dynamic, varied and well paid sphere. I know a lot of people in IT sphere who are constantly developing and have not reached the limit of development.

I studied Python. Made my first website. But I understud that python is not enough because I want to make not only working but also beautiful websites. Now I am studing HTML, CSS and Java-Script.

I love to study and open something new. But my main goal - is to expand my range of opportunities and influence. I would like to be able to choose work from different fields and conditions.

___

## Scills:
* Python;
* Django;
* HTML (Basic);
* CSS (Basic);
* VS Code, PyCharm;
* Git, GitHub;
* Autocad;
* MTV;


## Code example:
my first site, after [result_curses](https://nadtochaev-aleksandr.github.io/result_curses/?) only HTML and CSS \

my telegram bot: @Nadtochaev_scillbox_bot  \

some little part of my django site:  \

```
file models.py:
    class Nine_page(models.Model):
        p9_title=models.CharField(max_length=250)

            def __str__(self): # метод, который вместо id будет отображать поле p9_title, как более понятную и приёмлемую информацию
            return self.p9_title # тут в return и указывается какое поле необходимо возвращать вместо id

    class Photo(models.Model):
        obect=models.ForeignKey(Nine_page, on_delete=models.PROTECT)
        photo=models.ImageField(upload_to="catalog/img/", default='img')

        def __str__(self): # метод, который вместо id будет отображать поле obect, как более понятную и приёмлемую информацию
            return str(self.obect)+' '+str(self.pk) # тут в return и указывается какое поле необходимо возвращать вместо id
```

___
file views.py:
```
    def photo(request, object, pk):
        photos=Photo.objects.filter(obect__p9_title=object, pk=pk)
        portfolio = Nine_page.objects.get(p9_title=object)
        img = portfolio.photo_set.get(pk=pk)
        i = img.pk
        imgs=portfolio.photo_set.filter(obect__p9_title=object)
        len_obect_photo_list=len(imgs)
        first_photo_obect=imgs[0]
        last_photo_obect=imgs[len_obect_photo_list-1]
        l=i-1
        r=i+1
        context={'photos':photos, 'img':img, 'portfolio':portfolio, 'l':l, 'r':r,
                'imgs':imgs, 'len_obl':len_obect_photo_list,
                'first_photo':first_photo_obect, 'last_photo':last_photo_obect
                }
        return render(request, 'catalog/photo.html', context)
```
___
file urls.py:

```
    from django.urls import path
    from .views import *

    urlpatterns = [
        path('', main_page),
        path('second/', second_page),
        path('therd/', therd_page),
        path('4th/', fourth_page),
        path('5th/', fifth_page),
        path('6th/', sixth_page),
        path('7th/', seventh_page),
        path('8th/', eighth_page),
        path('9th/', ninth_page),
        path("9th/<str:object>/", object_page, name='object'),
        path('9th/<str:object>/<int:pk>', photo, name='photos'),
        path('10th/', tenth_page),
        path('11th/', eleventh_page),
        path('form/', form),
    ]
```

## Experience:
* construction master JSC "Gomelpromstroy" branch office "SU-61" - 08.2014-02.2016;
* production and technical department engineer JSC "Gomelpromstroy" branch office "SU-61" - 03.2016-12.2016;
* Head of production and technical department JSC "Gomelpromstroy" branch office "SU-61" - 01.2017-04.2017;
* Engineer of customer service JSC "Gazprom transgaz Belarus" - 05.2017 - now;

## Education:
* Belarusian state university of transport - 2009-2014 - civil engineer
* Belarusian state university of transport - 2014-2016 - master dergee (Master of Engineering Science)
* Academy of Public Administration under the President of the Republic of Belarus - economist manager
* IT OverOne - python developer

## Languages:
* English: A2-B1;
* Italian: B2;
* Russian: native;
* Belorussian: native;