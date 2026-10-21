# Uruchomienie na produkcji
W celu uruchomienia aplikacji należy zainstalować oprogramowanie Docker, a następnie wykonać polecenia:
```bash
docker compose -f docker-compose.prod.yml build
docker compose -f docker-compose.prod.yml up -d
```
Po chwili aplikacja powinna zostać uruchomiona. Z utworzonym domyślnym kontem administratora.

W celu zatrzymania aplikacji należy wykonać polecenie:
```bash
docker compose -f docker-compose.prod.yml down
```

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
