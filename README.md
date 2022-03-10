# TMask_Graylog_Windows_Security - Open Source

Graylog -> Syslog Security


========================

Nezbędne narzędzia:

- [Graylog](https://github.com/TMaskpl/TMask_Graylog_Windows_Security/blob/main/docker-compose.yml)
- [NXlog](https://nxlog.co/products/nxlog-community-edition/download)
- [Sysmon](https://docs.microsoft.com/en-us/sysinternals/downloads/sysmon)

-----------------------------

Uruchamiamy Graylog

Tworzymy Input


![2022-03-10_12-31_input](https://user-images.githubusercontent.com/75216446/157655203-d7ad1f5a-171c-400b-8f9d-6b58830c263f.png)


Tworzymy Rules Stream dla Windows Security Events

![2022-03-10_12-33_WindowsSecurityEvents](https://user-images.githubusercontent.com/75216446/157655333-7fd62b89-f0c9-45ed-beb3-245da4fd013f.png)


Windows Sysmon Events

![2022-03-10_12-34WindowsSysmon](https://user-images.githubusercontent.com/75216446/157655438-1968395c-9a06-44e4-b9bf-7e302059f84d.png)


Na docelowym systemie Windows instalujemy NXLog i Sysmon, przesyłamy wybrane na serwer Graylog

Następnie na Graylog tworzymy odpowiednie Alerty które po wykryciu interesującej nas informacji w logach prześlą do nas maila

# Dodanie użytkownika do grypy Administratorzy

![2022-03-10_12-49-addAdminGroup](https://user-images.githubusercontent.com/75216446/157656746-d1aea2b3-e45a-45c7-add0-1071a2d53e38.png)


# Podejrzane polecenie Powershell

![2022-03-10_12-50_PodejrzanyPowershell](https://user-images.githubusercontent.com/75216446/157656802-69999520-1814-47d2-8667-afdcdce69987.png)


# I wiele wiele innych

![2022-03-10_12-52_Alerts](https://user-images.githubusercontent.com/75216446/157656868-26852fec-ec69-429c-8d0f-be05ea025f34.png)


Wystarczy przesłać logi wyłąpać interesującą nas frazę i stworzyć powiadomienie mailowe. U mnie sprawdza się idealnie :)
