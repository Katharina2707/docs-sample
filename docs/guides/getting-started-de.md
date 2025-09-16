# Erste Schritte mit der User API

Dieses Dokument erklärt Ihnen, wie Sie sich authentifizieren und Ihre erste API-Anfrage stellen können, um Benutzerdaten abzurufen oder zu erstellen.

## Authentifizierung

Um die User API verwenden zu können, müssen Sie sich authentifizieren.
Erstellen Sie einen API-Schlüssel, bewahren Sie ihn sicher auf und teilen Sie ihn mit niemandem.

Für jede API-Anfrage müssen Sie Ihren API-Schlüssel in einem Authentifizierungs-Header angeben.
Das Format sieht wie folgt aus:
```yaml
X-API-Key: publicprefix.secret
```

## Ihre erste API-Anfrage stellen
### Alle Benutzer abrufen
Verwenden Sie `GET /v1/users`, um eine Liste aller Benutzer abzurufen, einschließlich der Benutzer-ID, des Namens und der E-Mail-Adresse. Sie müssen auch Ihren API-Schlüssel angeben:
```yaml
curl -X GET https://your-api-domain.com/v1/users \
  -H "X-API-Key: publicprefix.secret"
```

### Einen neuen Benutzer erstellen
Verwenden Sie `POST /v1/users`, um einen neuen Benutzer hinzuzufügen. Um einen neuen Benutzer zu erstellen, folgen Sie dem [User schema](../reference/users.md#User-schema) und geben Sie alle erforderlichen Felder wie Benutzer-ID, Name und E-Mail-Adresse an.
Auch hier müssen Sie Ihren API-Schlüssel angeben. Zum Beispiel:

```yaml
curl -X POST https://your-api-domain.com/v1/users \
  -H "Content-Type: application/json" \
  -H "X-API-Key: publicprefix.secret" \
  -d '{
    "id": "12345",
    "name": "Jane Doe",
    "email": "jane.doe@example.com"
  }'
```
Sie erhalten eine Bestätigung, wenn der Benutzer erfolgreich hinzugefügt wurde.



**Note:**
- Proper nouns stay english (User API, User schema)
- Established english words for developers stay english (Header)
- Code and filepaths stay english (`X-API-Key: publicprefix.secret`, `POST /v1/users`)


