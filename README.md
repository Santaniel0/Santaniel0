<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
  <img alt="Santanielo — бэкенд и инфраструктура" src="assets/header-light.svg" width="100%">
</picture>

Пишу на Go и Python. Больше всего нравятся задачи на стыке кода и инфраструктуры: сети, данные, деплой, восстановление после сбоев.

### Проекты

<table>
<tr>
<td width="50%" valign="top">
<b><a href="https://github.com/Santaniel0/normokontrol">normokontrol</a></b><br>
Проверяет ВКР и курсовые в .docx по ГОСТ 7.32 и ставит замечания прямо в документ примечаниями Word. Объясняет причину: «шрифт пришёл из стиля „Обычный“, исправьте стиль, а не 41 абзац».<br>
<sub>Go · OOXML · ГОСТ 7.32-2017</sub>
</td>
<td width="50%" valign="top">
<b><a href="https://github.com/Santaniel0/fwreach">fwreach</a></b><br>
Показывает, что на самом деле открыто наружу на сервере с Docker. Моделирует путь пакета через iptables и nftables и объясняет, почему правило ufw его не видит.<br>
<sub>Go · netfilter · Docker</sub>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<b><a href="https://github.com/Santaniel0/pg-copycheck">pg-copycheck</a></b><br>
Находит все строки CSV, на которых упадёт <code>COPY</code> в PostgreSQL, за один проход и без подключения к базе. Делит файл на чистый и отбракованный.<br>
<sub>Go · PostgreSQL · потоковая обработка</sub>
</td>
<td width="50%" valign="top">
<b><a href="https://github.com/Santaniel0/dns-cutover">dns-cutover</a></b><br>
Проверка перед сменой NS-серверов домена. Сравнивает старые и новые серверы запись за записью, ловит потерянный DKIM, MX за прокси и забытый DS у регистратора.<br>
<sub>Go · DNS · DNSSEC</sub>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<b><a href="https://github.com/Santaniel0/uncached">uncached</a></b><br>
Объясняет, почему <code>go test</code> в CI не взял результат из кэша: какой файл, переменная или флаг. Чинит самую частую причину, mtime после <code>git clone</code>.<br>
<sub>Go · go toolchain · CI</sub>
</td>
<td width="50%" valign="top">
<b><a href="https://github.com/Santaniel0/yandex-backup-under-test">yandex-backup-under-test</a></b><br>
Проверяет, что бэкап PostgreSQL в Yandex Cloud действительно восстанавливается: поднимает копию, сверяет данные и версии файлов в Object Storage, убирает за собой.<br>
<sub>Python · Terraform · Yandex Cloud</sub>
</td>
</tr>
</table>

### Документация Yandex Cloud

- [Что делать при утечке статического ключа доступа](https://github.com/yandex-cloud/docs/pull/1118) · `принят`
- [Защита резервных копий от удаления и перезаписи](https://github.com/yandex-cloud/docs/pull/1119) · `на ревью`
- [Проверка восстановления PostgreSQL и вложений Object Storage](https://github.com/yandex-cloud/docs/pull/1233) · `черновик`

### Стек

<img src="https://skillicons.dev/icons?i=go,python,postgres,redis,terraform,linux,nginx,bash,githubactions" height="36" alt="Go, Python, PostgreSQL, Redis, Terraform, Linux, nginx, Bash, GitHub Actions">
