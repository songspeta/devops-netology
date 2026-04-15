# devops-netology


DevOps Netology Course VCS

### Файл .gitignore для Terraform

Создан файл `terraform/.gitignore`.

```gitignore
# Terraform files
*.tfstate
*.tfstate.*
*.tfvars
*.tfvars.json

# Crash logs
.crash.log
.crash.*

# Directory for plugins
.terraform/
.terraform.lock.hcl

# CLI configuration files
.terraformrc
terraform.rc

# Override files
*.override.tf
*.override.tf.json

# Include tfplan files
*tfplan*

# Ignore CLI configuration files
~/.terraform.d/
```

**Расшифровка правил:**

| Правило | Что игнорируется |
|---------|------------------|
| `*.tfstate` | Все файлы, в имени которых есть `.tfstate` (например: `main.tfstate`, `prod.tfstate`) |
| `*.tfstate.*` | Все файлы, содержащие `.tfstate.` с любым расширением после (например: `main.tfstate.backup`) |
| `*.tfvars` | Все файлы с расширением `.tfvars` в любом месте репозитория |
| `.terraform/` | Директория `.terraform` и всё её содержимое (слэш в конце означает папку) |
| `.crash.log` | Файл с точным именем `.crash.log` |
| `.crash.*` | Все файлы, начинающиеся с `.crash.` (любое расширение) |
| `*.override.tf` | Все файлы, содержащие `.override.tf` в имени |
| `*tfplan*` | Все файлы, в имени которых есть подстрока `tfplan` (в любом месте) |
| `~/.terraform.d/` | Директория `.terraform.d` в домашней директории пользователя |
| `.terraformrc` | Файл с точным именем `.terraformrc` в корне репозитория |

**Спецсимволы:**
- `*` (звёздочка) — заменяет ноль или более любых символов
- `/` (слэш) в конце — указывает, что это директория
- `.` (точка) в начале — скрытые файлы/директории
- `~` (тильда) — домашняя директория пользователя