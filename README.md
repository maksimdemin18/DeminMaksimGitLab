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
   #          1. If provided manually (either via `GITLAB_ROOT_PASSWORD` environment variable or via `gitlab_rails['initial_root_password']` setting in `gitlab.rb`, it was provided before database was seeded for the first time (usually, the 
   first reconfigure run).
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


### Задание 2

`Приведите ответ в свободной форме........`

1. `git clone https://github.com/netology-code/sdvps-materials.git`
```
Cloning into 'sdvps-materials'...
remote: Enumerating objects: 97, done.
remote: Total 97 (delta 0), reused 0 (delta 0), pack-reused 97 (from 1)
Receiving objects: 100% (97/97), 28.22 KiB | 28.22 MiB/s, done.
Resolving deltas: 100% (38/38), done
```
2. `cd sdvps-materials`
3. `git remote rename origin upstream`
4. `git remote add origin git@gitlab.localdomain:root/netology-gitlab.git`
5. `git push -u origin main --force-with-lease`
6. ` git push origin --tags`
7. `git remote -v`
```
origin	git@gitlab.localdomain:root/netology-gitlab.git (fetch)
origin	git@gitlab.localdomain:root/netology-gitlab.git (push)
upstream	https://github.com/netology-code/sdvps-materials.git (fetch)
upstream	https://github.com/netology-code/sdvps-materials.git (push)
```
8. <img width="3840" height="3240" alt="image" src="https://github.com/user-attachments/assets/87494567-b95e-42e2-85d5-d0330e14ecb4" />


9. [.gitlab-ci.yml](.gitlab-ci.yml)

### Задание 3



