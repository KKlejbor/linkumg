# Uruchomienie na produkcji
W celu uruchomienia aplikacji należy zainstalować oprogramowanie Docker oraz narzędzie
docker-compose następnie wykonać polecenia:
```sh
docker-compose build -f docker-compose.prod.yml
docker-compose up -d
```
Po chwili aplikacja powinna zostać uruchomiona. Z utworzonym domyślnym kontem administratora. 

W celu zalogowania się jako administrator trzeba wykorzystać dane logowania:
```
login: admin 
hasło: password
```

Domyślnie dostęp do aplikacji zabezpieczony jest hasłem po stronie serwera nginx. 
Dane logowania:
```
login: user
hasło: Ku5Q4!g.
```
W celu dezaktywacji hasła należy w pliku nginx.conf usunąć linię zawierającą konfigurację `auth_basic*` i ponownie przebudować aplikację przy pomocy powyższych komend narzędzia docker-compose. 
