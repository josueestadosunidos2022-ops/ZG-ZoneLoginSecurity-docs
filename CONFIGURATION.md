# ZoneLoginSecurity 1.1.3 / 1.0.3 — configuration / configuración

## English

Server files are generated under `config/zoneloginsecurity/`. Stop the server and back up the persistent account database, server identity and configuration before changing releases. Never upload those private files to GitHub or CurseForge. Invalid or weakened security configuration is rejected by the server rather than silently allowing login.

| File | Main controls |
|---|---|
| `general.toml` | `enabled`, `require_client`, `login_timeout_seconds` |
| `registration.toml` | Console invitation codes, length, expiry, failed attempts, single use and required players |
| `credentials.toml` | Minimum password length, Argon2id and weak-password rejection |
| `login_protection.toml` | Before-world admission and TLS requirement |
| `sessions.toml` | Maximum duration, simultaneous sessions and revocation on password change |
| `administration.toml` | Temporary console OP `default_minutes`, `maximum_minutes`, protected permission nodes |
| `permissions.toml` | Authentication and console-only administration |
| `storage.toml` | SQLite engine, backup interval/retention, migration backup; some settings need restart |
| `audit.toml` | Auditing, masked IP and no secrets in logs |
| `accounts_control.toml` | Account lock overrides; legacy IP allowlists no longer authorize login |
| `messages_es.toml` | Spanish account lock message |

The database is world data at `data/zoneloginsecurity/accounts.sqlite`, not a public TOML. `/zlogin reload` validates supported policy changes; do not rotate or replace the server's private identity during a routine mod update. The client bundles a public SHA-256 certificate fingerprint in `zoneloginsecurity/server-public.sha256`; a local explicit pin can override it, and mismatch blocks the connection. `/zlogin admin status` checks temporary administrative authorization. Grant OP with `op Player` **from the server console after that player logs in**; `/zlogin admin revoke` and `deop Player` withdraw access.

## Español

Los archivos del servidor se generan en `config/zoneloginsecurity/`. Detén el servidor y respalda base de cuentas, identidad persistente y configuración antes de actualizar. No subas estos archivos privados a GitHub ni CurseForge. El servidor rechaza configuraciones inválidas o que debiliten controles obligatorios.

| Archivo | Uso principal |
|---|---|
| `general.toml` | Activación, cliente requerido y plazo de login |
| `registration.toml` | Códigos de invitación de consola, duración, intentos y usuarios requeridos |
| `credentials.toml` | Longitud mínima, Argon2id y bloqueo de contraseñas débiles |
| `login_protection.toml` | Admisión antes del mundo y TLS obligatorio |
| `sessions.toml` | Duración, sesiones simultáneas y revocación al cambiar contraseña |
| `administration.toml` | Minutos de OP temporal y nodos protegidos |
| `permissions.toml` | Autenticación y administración desde consola |
| `storage.toml` | SQLite y respaldo/retención; algunos cambios requieren reinicio |
| `audit.toml` | Auditoría, IP oculta y secretos fuera del log |
| `accounts_control.toml` | Bloqueo de cuentas; listas IP antiguas no autorizan login |
| `messages_es.toml` | Mensaje de bloqueo en español |

La base de cuentas está en los datos del mundo `data/zoneloginsecurity/accounts.sqlite`, no en un TOML público. `/zlogin reload` valida cambios admitidos. No cambies la identidad privada del servidor durante una actualización normal. El cliente incluye una huella pública SHA-256; una huella local explícita puede sustituirla y si no coincide se deniega la conexión. Desde consola y con el jugador ya autenticado usa `op Jugador` para OP temporal; consulta `/zlogin admin status` y revoca con `/zlogin admin revoke` o `deop Jugador`.

