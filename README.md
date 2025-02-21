# PowerShell Naming Conventions

PowerShell follows specific **naming conventions** for variables, functions, cmdlets, and other elements. While PowerShell is case-insensitive, it is recommended to follow these conventions for consistency and readability.

---

## 1. Variable Naming (`$camelCase`)
- Variables **should use camelCase** (`$myVariable`).
- Prefer descriptive names instead of single-letter names.
- Avoid reserved words and special characters (`?`, `&`, etc.).
- Use meaningful prefixes when necessary (e.g., `$isEnabled`, `$userName`).

**Correct:**
```powershell
$firstName = "John"
$totalCount = 10
$isRunning = $true
```

**Avoid:**
```powershell
$First_name = "John"   # Underscores are not typical
$x = 10                # Too generic
$MyVar = "Test"        # Inconsistent casing
```

---

## 2. Function Naming (`PascalCase` with Verb-Noun)
- Functions **should use PascalCase** (`Get-Data`).
- Follow the **Verb-Noun** convention (`Get-`, `Set-`, `Test-`, etc.).
- Use **approved verbs** from `Get-Verb` for consistency.

**Correct:**
```powershell
function Get-UserInfo {
    param([string]$userName)
    "Fetching info for $userName"
}
```

**Avoid:**
```powershell
function getuserinfo {}    # Not PascalCase
function Fetch-User {}     # "Fetch" is not an approved verb
function user-get {}       # Incorrect order (should be Verb-Noun)
```

**Common Verbs:**
- `Get-` (retrieve data)
- `Set-` (update or modify data)
- `New-` (create an item)
- `Remove-` (delete an item)
- `Test-` (validate something)
- `Start-`, `Stop-`, `Restart-` (control processes)

To list all approved verbs:
```powershell
Get-Verb
```

---

## 3. Cmdlet Naming (Verb-Noun)
If you're defining a custom cmdlet in PowerShell, follow the **Verb-Noun** pattern, similar to function names.

**Correct:**
```powershell
function Get-EmployeeRecord { }
function Set-ConfigValue { }
```

**Avoid:**
```powershell
function Employee-Get { }  # Incorrect order
function fetchRecord { }   # Unapproved verb
```

---

## 4. Parameter Naming (`camelCase`)
- Parameters **should use camelCase** (`$userName`).
- Avoid abbreviations unless well-known.

**Correct:**
```powershell
function Get-UserInfo {
    param (
        [string]$userName,
        [int]$age
    )
    "User: $userName, Age: $age"
}
```

**Avoid:**
```powershell
param([string]$User_Name)   # Underscores are unnecessary
param([string]$un)          # "un" is unclear (use full words)
```

---

## 5. Script Naming (`PascalCase.ps1`)
- PowerShell script files (`.ps1`) should use **PascalCase**.
- Use descriptive names with dashes.

**Correct:**
```
Install-Software.ps1
Backup-Database.ps1
Start-WebServer.ps1
```

**Avoid:**
```
installsoftware.ps1    # Hard to read
backup_database.ps1    # Uses underscores (uncommon)
startwebserver.ps1     # Not PascalCase
```

---

## 6. Module Naming (`PascalCase.psm1`)
- PowerShell module files (`.psm1`) should use **PascalCase**.

**Correct:**
```
MyCustomModule.psm1
NetworkUtilities.psm1
```

**Avoid:**
```
mycustommodule.psm1    # Not PascalCase
network_utilities.psm1 # Uses underscores
```

---

## 7. Alias Naming (`Short & Meaningful`)
- Use short, clear aliases that map well to the original command.
- Avoid non-descriptive names.

**Correct:**
```powershell
Set-Alias -Name gci -Value Get-ChildItem
```

**Avoid:**
```powershell
Set-Alias -Name abc -Value Get-Process  # "abc" is not meaningful
```

---

## 8. Constant Naming (`PascalCase`, `$global:` if needed)
- Constants are typically all uppercase or PascalCase.
- If global, use `$global:`.

**Correct:**
```powershell
$global:MaxRetries = 5
$DefaultTimeout = 30
```

**Avoid:**
```powershell
$max_retries = 5    # Uses underscores (not typical)
$defaulttimeout = 30 # Not PascalCase
```

---

## 9. Enum Naming (`PascalCase` for Type and Values)
**Correct:**
```powershell
enum Status {
    Active
    Inactive
    Pending
}
```

**Avoid:**
```powershell
enum status { active, inactive, pending }  # Not PascalCase
```

---

## 10. Class Naming (`PascalCase` for Class and Properties)
**Correct:**
```powershell
class User {
    [string]$Name
    [int]$Age
}
```

**Avoid:**
```powershell
class user { [string]$name; [int]$age }  # Not PascalCase
```

---

## Summary Table

| **Item**        | **Naming Convention**           | **Example**          |
|---------------|---------------------------|------------------|
| **Variables**  | `camelCase`                | `$firstName`     |
| **Functions**  | `PascalCase`, `Verb-Noun`  | `Get-UserInfo`   |
| **Cmdlets**    | `Verb-Noun`                | `Set-Config`     |
| **Parameters** | `camelCase`                | `$userName`      |
| **Scripts**    | `PascalCase.ps1`           | `Install-Tool.ps1` |
| **Modules**    | `PascalCase.psm1`          | `NetworkTools.psm1` |
| **Aliases**    | Short & meaningful         | `Set-Alias gci Get-ChildItem` |
| **Constants**  | `PascalCase` / uppercase   | `$MaxRetries` / `$global:TIMEOUT` |
| **Enums**      | `PascalCase`               | `enum Status { Active, Inactive }` |
| **Classes**    | `PascalCase`               | `class User { [string]$Name }` |

---
### Final Thoughts
Following PowerShell's naming conventions helps ensure that your scripts are:
- **Consistent**
- **Readable**
- **Maintainable**
