# Практическая работа №5 - Threat Hunting

**Выполнил студент группы ББМО-02-23 Васильев Г.М.**

Вся информация по установке и отладке была взята из практической работы №3

**В работе были использованы 2 Виртуальнае машины на базе операционной системы Ubuntu v22.04.4 под сервер и агент XDR Wazuh**

Демонстрация подключения агента к серверу:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/19.JPG)

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/18.JPG)

# IDS Suricata

Разворначиваем IDS Суриката:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/1.JPG)

Внесение изменений для дальнейшего сбора логов suricata в конфиг xdr wazuh:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/2.JPG)

На защищаемом сервере поднимаем Apache:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/3.JPG)

# Сканер уязвимостей NIKTO

Установка сканер уязвимостей Nikto:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/4.JPG)

Устанавливает интерпретатор Perl и систему контроля версий Git без необходимости подтверждения действий пользователем.:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/5.JPG)

Запустим сканер уязвимостей Nikto:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/6.JPG)

События от сурикаты в SIEM:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/16.JPG)

Более подробное рассмотрение одного из логов:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/17.JPG)

# Yara

Скачивание необходимых пакетов:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/7.JPG)

Команда для устанавливки всех необходимых инструментов и библиотек для сборки и разработки программного обеспечения, включая YARA:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/8.JPG)

Команда конфигурирует сборку YARA с поддержкой специфичных форматов файлов и библиотек:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/9.JPG)

Команда для использования параллельной сборки может сократить время, необходимое для завершения процесса компиляции:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/10.JPG)

Начало полной установки Yara:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/11.JPG)

Создадим конфигурационный файл активного реагирования под утилиту yara:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/20.JPG)

Добавление действий в конфигурационный файл действий регаирования в XDR wazuh:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/15.JPG)

Просмотр сработавших Yara правил в истории логов XDR Wazuh:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/12.JPG)

Болееподробный просмотр одного из сработавших правил:

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/13.JPG)

![image](https://github.com/Archangel15520/sssl5/blob/main/Screenshot/14.JPG)


