# Домашнее задание к занятию "`GitLab`" - `Дёмин максим`


### Задание 1
Что нужно сделать:

Разверните GitLab локально, используя Vagrantfile и инструкцию, описанные в этом репозитории.
Создайте новый проект и пустой репозиторий в нём.
Зарегистрируйте gitlab-runner для этого проекта и запустите его в режиме Docker. Раннер можно регистрировать и запускать на той же виртуальной машине, на которой запущен GitLab.
В качестве ответа в репозиторий шаблона с решением добавьте скриншоты с настройками раннера в проекте.

### Задание 2
Что нужно сделать:

Запушьте репозиторий на GitLab, изменив origin. Это изучалось на занятии по Git.
Создайте .gitlab-ci.yml, описав в нём все необходимые, на ваш взгляд, этапы.
В качестве ответа в шаблон с решением добавьте:

файл gitlab-ci.yml для своего проекта или вставьте код в соответствующее поле в шаблоне;
скриншоты с успешно собранными сборками.
Дополнительные задания* (со звёздочкой)
Их выполнение необязательное и не влияет на получение зачёта по домашнему заданию. Можете их решить, если хотите лучше разобраться в материале.

### Задание 3*
Измените CI так, чтобы:

этап сборки запускался сразу, не дожидаясь результатов тестов;
тесты запускались только при изменении файлов с расширением *.go.
В качестве ответа добавьте в шаблон с решением файл gitlab-ci.yml своего проекта или вставьте код в соответсвующее поле в шаблоне.
   


### Задание 1

`Приведите ответ в свободной форме........`

1. `sudo apt install virtualbox`
2. `sudo apt install -y ./vagrant_2.4.9-1_amd64.deb`
3. `vagrant init`
4. `VAGRANT_EXPERIMENTAL="disks" vagrant up`
   ```
    default: Thank you for installing GitLab!
    default: GitLab should be available at http://gitlab.localdomain
    default: 
    default: For a comprehensive list of configuration options please see the Omnibus GitLab readme
    default: https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/README.md
   ```
5. `vagrant ssh -- sudo cat /etc/gitlab/initial_root_password`
   ```
   # WARNING: This value is valid only in the following conditions
#          1. If provided manually (either via `GITLAB_ROOT_PASSWORD` environment variable or via `gitlab_rails['initial_root_password']` setting in `gitlab.rb`, it was provided before database was seeded for the first time (usually, the first reconfigure run).
#          2. Password hasn't been changed manually, either via UI or via command line.
#
#          If the password shown here doesn't work, you must reset the admin password following https://docs.gitlab.com/ee/security/reset_user_password.html#reset-your-root-password.

Password:
   ```
6. авторизуемся и создаем репозиторий
![photo_2026-01-06_14-48-13](https://github.com/user-attachments/assets/310f9ecc-655d-469f-8a82-321817f2c376)
![photo_2026-01-06_14-51-14](https://github.com/user-attachments/assets/84d4fee8-dcd0-40ee-a13e-65fda013a1f9)

7. Добавляем runner
![photo_2026-01-06_14-53-28](https://github.com/user-attachments/assets/95444e68-690e-4edc-8bb5-3ce44aece0b4)
![photo_2026-01-06_14-55-51](https://github.com/user-attachments/assets/20d4f7b5-3285-40d7-8355-a5ddedd1f0de)
![photo_2026-01-07_12-59-55](https://github.com/user-attachments/assets/8beae395-563a-45d9-8134-821dadc5cc4a)



```
Поле для вставки кода...
....
....
....
....
```

`При необходимости прикрепитe сюда скриншоты
![Название скриншота 1](ссылка на скриншот 1)`


---

### Задание 2

`Приведите ответ в свободной форме........`

1. `Заполните здесь этапы выполнения, если требуется ....`
2. `Заполните здесь этапы выполнения, если требуется ....`
3. `Заполните здесь этапы выполнения, если требуется ....`
4. `Заполните здесь этапы выполнения, если требуется ....`
5. `Заполните здесь этапы выполнения, если требуется ....`
6. 

```
Поле для вставки кода...
....
....
....
....
```

`При необходимости прикрепитe сюда скриншоты
![Название скриншота 2](ссылка на скриншот 2)`


---

### Задание 3

`Приведите ответ в свободной форме........`

1. `Заполните здесь этапы выполнения, если требуется ....`
2. `Заполните здесь этапы выполнения, если требуется ....`
3. `Заполните здесь этапы выполнения, если требуется ....`
4. `Заполните здесь этапы выполнения, если требуется ....`
5. `Заполните здесь этапы выполнения, если требуется ....`
6. 

```
Поле для вставки кода...
....
....
....
....
```

`При необходимости прикрепитe сюда скриншоты
![Название скриншота](ссылка на скриншот)`


