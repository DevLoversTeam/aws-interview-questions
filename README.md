<h1>
  AWS <img src="./assets/aws.svg" width="40" height="40" />
</h1>

<h2>Найпопулярніші запитання та відповіді на співбесіді з AWS</h2>

<details>
<summary>1. Що таке AWS?</summary>

#### AWS

**AWS (Amazon Web Services)** — це хмарна платформа від Amazon, яка надає
інфраструктурні та прикладні сервіси через інтернет за моделлю pay-as-you-go.

AWS дозволяє запускати застосунки без купівлі власного "заліза": обчислення,
бази даних, сховища, мережі, аналітика, AI/ML та безпека доступні як керовані
сервіси.

**Коротко:**

- AWS — це публічна хмарна платформа Amazon.
- Дає сервери, БД, сховища, мережі й інші сервіси "на вимогу".
- Оплата за фактичне використання ресурсів.

</details>

<details>
<summary>2. Які основні переваги використання AWS?</summary>

#### AWS

Основні переваги AWS:

1. **Масштабованість**: ресурси можна швидко збільшувати або зменшувати під
   навантаження.
2. **Глобальна інфраструктура**: регіони та зони доступності по всьому світу.
3. **Надійність і відмовостійкість**: можливість будувати архітектури з високою
   доступністю.
4. **Швидкість запуску**: нові середовища розгортаються за хвилини.
5. **Pay-as-you-go**: оплата лише за реально використані ресурси.
6. **Безпека**: потужний стек сервісів безпеки й контролю доступу.

**Коротко:**

- AWS дає гнучке масштабування і швидкий time-to-market.
- Дозволяє будувати надійні global-системи.
- Зменшує capex і переводить витрати в керований opex.

</details>

<details>
<summary>3. Які проблеми вирішує AWS?</summary>

#### AWS

AWS вирішує типові інженерні та бізнесові проблеми:

- відмова від закупівлі й обслуговування власної інфраструктури;
- повільний запуск нових середовищ і продуктів;
- складне масштабування під пікові навантаження;
- низька відмовостійкість при single-datacenter підході;
- ручні та нестабільні деплої без автоматизації;
- відсутність централізованих інструментів безпеки, моніторингу й аудиту.

**Коротко:**

- AWS прибирає операційну рутину навколо "заліза".
- Дозволяє швидше релізити і стабільніше масштабуватися.
- Дає вбудовані інструменти для безпеки, моніторингу та відновлення.

</details>

<details>
<summary>4. Які основні моделі хмарних сервісів (IaaS, PaaS, SaaS)?</summary>

#### AWS

Основні моделі хмарних сервісів:

- **IaaS (Infrastructure as a Service)**: провайдер дає базову інфраструктуру
  (compute, storage, network), а ви керуєте ОС, middleware і застосунком.
- **PaaS (Platform as a Service)**: провайдер додатково керує платформою
  виконання, а ви фокусуєтесь на коді та даних.
- **SaaS (Software as a Service)**: готовий продукт, яким користуються через
  веб-інтерфейс або API, без керування інфраструктурою.

Принцип простий: від IaaS до SaaS зростає рівень абстракції і зменшується обсяг
операційної відповідальності клієнта.

**Коротко:**

- IaaS: більше контролю, більше операційної роботи.
- PaaS: баланс між контролем і швидкістю розробки.
- SaaS: мінімум адміністрування, фокус на бізнес-функції.

</details>

<details>
<summary>5. Що таке AWS Regions та Availability Zones?</summary>

#### AWS

- **AWS Region** — це окремий географічний регіон AWS (наприклад, `eu-central-1`
  або `us-east-1`), що складається з кількох дата-центрів.
- **Availability Zone (AZ)** — це ізольована зона всередині регіону з
  незалежним живленням, мережею та фізичною інфраструктурою.

Кожен регіон має щонайменше дві AZ, зазвичай більше. Для high availability
рекомендується розміщувати критичні компоненти мінімум у двох AZ одного
регіону.

**Коротко:**

- Region = географія розміщення.
- AZ = ізольована зона відмовостійкості в межах регіону.
- Продакшн-системи будують multi-AZ.

</details>

<details>
<summary>6. У чому різниця між Region та Availability Zone?</summary>

#### AWS

Різниця в рівні географії та ізоляції:

- **Region** — велика географічна локація AWS.
- **Availability Zone (AZ)** — окрема ізольована зона всередині одного Region,
  побудована як незалежний fault domain.

Region обирають за близькістю до користувачів, юридичними вимогами та ціною.
AZ використовують для відмовостійкості: сервіси розміщують у кількох AZ одного
регіону.

**Коротко:**

- Region = географічний рівень.
- AZ = рівень відмовостійкості всередині регіону.
- HA зазвичай досягають через multi-AZ у межах одного Region.

</details>

<details>
<summary>7. Що таке модель спільної відповідальності (Shared Responsibility Model) в AWS?</summary>

#### AWS

**Shared Responsibility Model** означає, що безпека в хмарі ділиться між AWS і
клієнтом:

- **AWS відповідає за безпеку хмари**: фізичні дата-центри, мережеву
  інфраструктуру та базові керовані сервіси.
- **Клієнт відповідає за безпеку в хмарі**: IAM-права, конфігурацію сервісів,
  шифрування даних, політики доступу й моніторинг.

Рівень відповідальності клієнта залежить від типу сервісу: у IaaS він вищий, у
PaaS/SaaS — нижчий.

**Коротко:**

- AWS захищає інфраструктуру платформи.
- Клієнт захищає свої дані, доступи та конфігурації.
- Чим більш керований сервіс, тим менше операційної відповідальності клієнта.

</details>

<details>
<summary>8. Що таке Infrastructure as Code (IaC)?</summary>

#### AWS

**Infrastructure as Code (IaC)** — це підхід, коли інфраструктура описується
кодом (шаблонами/маніфестами), а не створюється вручну через UI.

В AWS це найчастіше реалізують через CloudFormation, AWS CDK, Terraform.
Переваги IaC:

- повторюваність середовищ;
- контроль змін через Git;
- автоматизація розгортань у CI/CD;
- менше manual drift і людських помилок.

**Коротко:**

- IaC = інфраструктура як версійований код.
- Дає передбачувані деплої та audit trail.
- Базова практика для зрілого DevOps у AWS.

</details>

<details>
<summary>9. У чому різниця між горизонтальним і вертикальним масштабуванням?</summary>

#### AWS

- **Вертикальне масштабування (scale up/down)** — зміна потужності одного
  інстансу (більше CPU/RAM або менше).
- **Горизонтальне масштабування (scale out/in)** — додавання або зменшення
  кількості інстансів/нод.

Вертикальне масштабування простіше на старті, але має фізичну межу й часто
потребує downtime. Горизонтальне складніше архітектурно, зате краще для
відмовостійкості та еластичності.

**Коротко:**

- Вертикальне: "сильніший один сервер".
- Горизонтальне: "більше серверів".
- Для production web-систем частіше обирають горизонтальне масштабування.

</details>

<details>
<summary>10. Що таке AWS Well-Architected Framework і які його шість принципів?</summary>

#### AWS

**AWS Well-Architected Framework** — це набір best practices для проєктування,
оцінки й покращення хмарних архітектур.

Шість pillars:

1. **Operational Excellence**
2. **Security**
3. **Reliability**
4. **Performance Efficiency**
5. **Cost Optimization**
6. **Sustainability**

Framework застосовують як чекліст під час архітектурних review і технічного
планування.

**Коротко:**

- Well-Architected — стандарт якості архітектури в AWS.
- Складається з 6 pillars: Operations, Security, Reliability, Performance, Cost, Sustainability.
- Допомагає системно знаходити ризики і покращувати рішення.

</details>

<details>
<summary>11. Що таке AWS Free Tier і коли його варто використовувати?</summary>

#### AWS

**AWS Free Tier** — це набір безкоштовних лімітів на сервіси AWS, який дозволяє
знайомитись із платформою без значних витрат.

Типові сценарії використання:

- навчання та підготовка до співбесід/сертифікацій;
- лабораторні стенди й pet-проєкти;
- перевірка PoC перед production-рішенням.

Важливо контролювати ліміти й регіони: при перевищенні безкоштовного обсягу
починається стандартна тарифікація.

**Коротко:**

- Free Tier підходить для навчання, тестів і PoC.
- Не замінює production-бюджетування.
- Потрібен cost-контроль, щоб уникнути неочікуваних витрат.

</details>

<details>
<summary>12. Що таке IAM?</summary>

#### AWS

**IAM (Identity and Access Management)** — це сервіс AWS для керування
ідентичностями та доступом до ресурсів.

Через IAM ви визначаєте:

- хто може виконувати дії (користувач, роль, сервіс);
- які саме дії дозволені або заборонені;
- над якими ресурсами ці дії можна виконувати;
- за яких умов доступ надається.

IAM є базовим рівнем безпеки в AWS-акаунті.

```bash
aws iam list-users
aws iam list-roles
aws sts get-caller-identity
```

**Коротко:**

- IAM керує доступами в AWS.
- Працює через identity + policy модель.
- Основа безпечної багатокористувацької роботи в акаунті.

</details>

<details>
<summary>13. У чому різниця між IAM Users, Groups та Roles?</summary>

#### AWS

- **IAM User** — ідентичність для конкретної людини або legacy-сценарію з
  довгостроковими credential'ами.
- **IAM Group** — логічна група користувачів, до якої прикріплюють спільні
  permissions через policies.
- **IAM Role** — ідентичність без постійного пароля/ключів, яку тимчасово
  "assume" люди, сервіси або інші акаунти через STS.

Практика для production: мінімізувати використання User access keys і
переходити на roles + короткоживучі тимчасові credentials.

**Коротко:**

- User = конкретний користувач.
- Group = набір користувачів зі спільними правами.
- Role = тимчасовий доступ без постійних ключів.

</details>

<details>
<summary>14. Як працюють IAM policies?</summary>

#### AWS

**IAM policy** — це JSON-документ, який описує дозволи:

- `Effect` (`Allow` або `Deny`);
- `Action` (що можна робити);
- `Resource` (над чим можна робити);
- `Condition` (за яких умов).

Під час авторизації AWS обчислює всі релевантні політики. Важливе правило:
**explicit deny завжди має пріоритет над allow**.

Policies можуть бути:

- identity-based (на user/group/role);
- resource-based (на самому ресурсі, наприклад S3 bucket policy).

```bash
aws iam simulate-principal-policy \
  --policy-source-arn arn:aws:iam::123456789012:role/AppRole \
  --action-names s3:GetObject \
  --resource-arns arn:aws:s3:::my-bucket/*
```

**Коротко:**

- Policy = декларативні правила доступу у JSON.
- Доступ визначається комбінацією policy документів.
- `Deny` має найвищий пріоритет.

</details>

<details>
<summary>15. Що означає принцип найменших привілеїв (least privilege)?</summary>

#### AWS

Принцип **least privilege** означає надавати лише ті права, які потрібні для
конкретного завдання, і не більше.

Практичне застосування в AWS:

- уникати wildcard-дозволів (`*`) без критичної потреби;
- обмежувати доступ конкретними ресурсами;
- додавати умови (MFA, source IP, time-based access);
- регулярно переглядати й зменшувати надлишкові права.

Це знижує blast radius у разі компрометації облікового запису або сервісу.

**Коротко:**

- Мінімум прав для виконання роботи.
- Менше зайвих доступів = менший ризик інциденту.
- Права мають бути точкові, короткоживучі та регулярно рев'юватись.

</details>

<details>
<summary>16. Що таке MFA в AWS?</summary>

#### AWS

**MFA (Multi-Factor Authentication)** — це додатковий фактор автентифікації
поверх пароля/ключа (наприклад, TOTP або hardware token).

У AWS MFA особливо важливе для:

- root account;
- привілейованих IAM-користувачів;
- критичних операцій (через умови в IAM policies).

MFA суттєво зменшує ризик несанкціонованого доступу при витоку пароля.

```bash
aws iam list-mfa-devices --user-name alice
aws sts get-session-token --serial-number arn:aws:iam::123456789012:mfa/alice --token-code 123456
```

**Коротко:**

- MFA = другий фактор входу.
- Обов'язковий мінімум для root і адмінів.
- Підвищує безпеку навіть при компрометації пароля.

</details>

<details>
<summary>17. Що таке AWS KMS?</summary>

#### AWS

**AWS KMS (Key Management Service)** — керований сервіс для створення,
зберігання та керування криптографічними ключами.

KMS інтегрований з багатьма сервісами AWS (S3, EBS, RDS, Secrets Manager тощо)
і дозволяє:

- централізовано керувати ключами;
- контролювати доступ до операцій шифрування/дешифрування;
- вести аудит через CloudTrail;
- автоматизувати ротацію ключів (для підтримуваних типів).

```bash
aws kms list-keys
aws kms describe-key --key-id alias/aws/s3
aws kms encrypt --key-id alias/my-key --plaintext fileb://secret.txt
```

**Коротко:**

- KMS = централізоване керування ключами шифрування.
- Спрощує безпечне шифрування в AWS-сервісах.
- Дає контроль доступу й аудит криптооперацій.

</details>

<details>
<summary>18. Що таке envelope encryption?</summary>

#### AWS

**Envelope encryption** — це підхід, коли дані шифруються не напряму master
ключем, а через проміжний data key:

1. KMS генерує data key.
2. Дані шифруються цим data key локально в застосунку/сервісі.
3. Сам data key шифрується KMS master key і зберігається поруч із даними.

Це дає кращу продуктивність і масштабованість, бо великі обсяги даних
шифруються data key, а KMS використовується для захисту самого ключа.

**Коротко:**

- Дані шифруються data key.
- Data key додатково шифрується ключем KMS.
- Стандартний підхід для безпечного та масштабованого шифрування.

</details>

<details>
<summary>19. Що таке AWS Secrets Manager?</summary>

#### AWS

**AWS Secrets Manager** — це сервіс для безпечного зберігання, ротації та
видачі секретів (паролі БД, API keys, токени).

Ключові можливості:

- зберігання секретів у зашифрованому вигляді (KMS);
- контроль доступу через IAM;
- автоматична ротація для підтримуваних інтеграцій;
- отримання секретів програмно через API/SDK.

Секрети не повинні зберігатись у коді, Git-репозиторіях або змінних середовища
без контролю.

```bash
aws secretsmanager create-secret --name app/prod/db --secret-string '{"username":"app","password":"***"}'
aws secretsmanager get-secret-value --secret-id app/prod/db
```

**Коротко:**

- Secrets Manager централізує керування секретами.
- Підтримує шифрування, аудит і ротацію.
- Основний інструмент для secure secret lifecycle у AWS.

</details>

<details>
<summary>20. Що робити, якщо облікові ключі AWS були випадково опубліковані?</summary>

#### AWS

Якщо AWS access keys потрапили у публічний доступ, діяти треба негайно:

1. **Негайно деактивувати/видалити ключі** в IAM.
2. **Створити нові credentials** і оновити всі сервіси/CI.
3. **Перевірити CloudTrail** на підозрілі дії від моменту витоку.
4. **Оцінити blast radius**: які ресурси могли бути змінені/прочитані.
5. **Ротація пов'язаних секретів** (БД, токени, зовнішні API), якщо були доступні.
6. **Посилити захист**: перейти на IAM Roles, short-lived creds, увімкнути guardrails.

Додатково варто перевірити billing/anomaly detection, щоб швидко виявити
несанкціоноване використання ресурсів.

```bash
aws iam update-access-key --user-name compromised-user --access-key-id AKIA... --status Inactive
aws iam delete-access-key --user-name compromised-user --access-key-id AKIA...
aws cloudtrail lookup-events --lookup-attributes AttributeKey=Username,AttributeValue=compromised-user
```

**Коротко:**

- Ключі треба відкликати негайно.
- Після ротації обов'язкові аудит і розслідування.
- Довгостроково переходити від static keys до IAM Roles.

</details>

<details>
<summary>21. Як забезпечити захист даних у стані зберігання та під час передачі в AWS?</summary>

#### AWS

Для захисту даних в AWS застосовують два шари:

- **Data at rest (у стані зберігання)**:
  шифрування через KMS для S3, EBS, RDS, backups, snapshots;
  керування ключами, ротація, мінімальні доступи до decrypt-операцій.
- **Data in transit (під час передачі)**:
  TLS 1.2+ для зовнішнього і внутрішнього трафіку;
  HTTPS, mTLS (де потрібно), захищені VPN/Direct Connect канали.

Додатково:

- жорсткі IAM-політики та segmentation мережі;
- аудит доступу (CloudTrail, Config);
- DLP/класифікація даних і retention-політики.

```bash
aws s3api put-bucket-encryption --bucket my-bucket --server-side-encryption-configuration file://sse.json
aws ec2 create-ebs-default-kms-key-id --kms-key-id arn:aws:kms:eu-central-1:123456789012:key/abcd...
aws rds modify-db-instance --db-instance-identifier prod-db --storage-encrypted --apply-immediately
```

**Коротко:**

- At rest: шифрування даних і контроль ключів.
- In transit: TLS для всіх критичних з'єднань.
- Безпека даних = шифрування + IAM + аудит + мережеві контролі.

</details>

<details>
<summary>22. Що таке VPC?</summary>

#### AWS

**Amazon VPC (Virtual Private Cloud)** — це логічно ізольована віртуальна
мережа в AWS, де ви розміщуєте свої ресурси (EC2, RDS, ECS тощо) і керуєте
адресним простором, маршрутизацією та мережевою безпекою.

VPC дає повний контроль над мережею на рівні хмарної інфраструктури:
CIDR-блоки, subnet-и, таблиці маршрутів, шлюзи, політики доступу.

```bash
aws ec2 describe-vpcs
aws ec2 describe-subnets --filters Name=vpc-id,Values=vpc-1234567890abcdef0
aws ec2 describe-route-tables --filters Name=vpc-id,Values=vpc-1234567890abcdef0
```

**Коротко:**

- VPC = приватна мережа в межах AWS-акаунта.
- Дозволяє ізолювати і безпечно сегментувати інфраструктуру.
- Базовий будівельний блок мережевої архітектури в AWS.

</details>

<details>
<summary>23. Які основні компоненти VPC?</summary>

#### AWS

Основні компоненти VPC:

- **CIDR block** — адресний простір VPC;
- **Subnets** — сегменти мережі в конкретних AZ;
- **Route Tables** — правила маршрутизації;
- **Internet Gateway (IGW)** — доступ до інтернету для public subnet;
- **NAT Gateway/Instance** — вихід у інтернет з private subnet;
- **Security Groups** — stateful фільтрація на рівні ENI/інстансу;
- **Network ACL (NACL)** — stateless фільтрація на рівні subnet;
- **VPC Endpoints** — приватний доступ до сервісів AWS;
- **VPC Flow Logs** — журналювання мережевого трафіку.

**Коротко:**

- VPC складається з адресації, сегментації, маршрутизації та фаєрволів.
- IGW/NAT визначають інтернет-доступ.
- SG/NACL контролюють мережеву безпеку на різних рівнях.

</details>

<details>
<summary>24. Що таке subnet?</summary>

#### AWS

**Subnet** — це підмережа всередині VPC, тобто частина CIDR-діапазону VPC,
прив'язана до конкретної Availability Zone.

Ресурси запускаються саме в subnet-ах, а тип доступності (public/private)
визначається маршрутизацією та наявністю публічного маршруту через IGW.

**Коротко:**

- Subnet = сегмент VPC в межах однієї AZ.
- Через subnet-и роблять мережеву сегментацію середовищ.
- Тип subnet визначається route table, а не назвою.

</details>

<details>
<summary>25. У чому різниця між public і private subnet?</summary>

#### AWS

- **Public subnet** має маршрут до **Internet Gateway** (наприклад
  `0.0.0.0/0 -> igw-...`) і зазвичай використовується для ALB, bastion, NAT.
- **Private subnet** не має прямого маршруту до IGW; для вихідного доступу в
  інтернет використовує NAT Gateway/Instance або взагалі працює без інтернету.

Ключова різниця — не в назві subnet, а в таблиці маршрутів.

**Коротко:**

- Public subnet: є direct route до IGW.
- Private subnet: немає direct route до IGW.
- Різницю визначає маршрутизація, а не тип інстансу.

</details>

<details>
<summary>26. Що таке Internet Gateway?</summary>

#### AWS

**Internet Gateway (IGW)** — це керований шлюз, який прикріплюється до VPC і
забезпечує обмін трафіком між VPC та інтернетом.

Щоб ресурс був доступний з інтернету, потрібні:

- маршрут у route table до IGW;
- публічна IP-адреса (або EIP);
- коректні правила SG/NACL.

**Коротко:**

- IGW дає VPC вихід/вхід в інтернет.
- Працює разом із route table та публічними IP.
- Критичний компонент для public workloads.

</details>

<details>
<summary>27. Що таке NAT Gateway?</summary>

#### AWS

**NAT Gateway** — керований сервіс для вихідного інтернет-доступу з private
subnet без відкриття вхідних з'єднань з інтернету.

Типовий патерн:

1. NAT Gateway розміщується в public subnet.
2. Має Elastic IP.
3. Private subnet-и маршрутизують `0.0.0.0/0` на NAT Gateway.

```bash
aws ec2 create-nat-gateway --subnet-id subnet-public --allocation-id eipalloc-1234abcd
aws ec2 describe-nat-gateways --filter Name=vpc-id,Values=vpc-1234567890abcdef0
```

**Коротко:**

- NAT Gateway дає outbound internet для private subnet.
- Вхідний трафік з інтернету через нього не ініціюється.
- Стандартний production-підхід для приватних ворклоадів.

</details>

<details>
<summary>28. У чому різниця між NAT Instance і NAT Gateway?</summary>

#### AWS

- **NAT Instance** — EC2-інстанс, який ви самі адмініструєте
  (патчі, scaling, HA, моніторинг).
- **NAT Gateway** — fully managed сервіс AWS з кращою операційною простотою.

NAT Instance може бути дешевшим у вузьких сценаріях, але має вищий operational
risk. Для більшості production-систем рекомендований NAT Gateway.

**Коротко:**

- NAT Instance: більше контролю, більше ручної роботи.
- NAT Gateway: менше операційного навантаження, краща надійність.
- У production зазвичай обирають NAT Gateway.

</details>

<details>
<summary>29. Що таке route tables?</summary>

#### AWS

**Route Table** — набір правил маршрутизації для subnet у VPC.

Кожен запис визначає:

- destination CIDR (куди йде трафік);
- target (через що йде трафік: local, IGW, NAT, peering, TGW, endpoint).

Саме route table визначає, як subnet взаємодіє з іншими мережами та інтернетом.

```bash
aws ec2 describe-route-tables --route-table-ids rtb-1234567890abcdef0
aws ec2 create-route --route-table-id rtb-1234567890abcdef0 --destination-cidr-block 0.0.0.0/0 --gateway-id igw-1234567890abcdef0
```

**Коротко:**

- Route table керує напрямком мережевого трафіку.
- Прив'язується до subnet.
- Від маршрутизації залежить public/private поведінка мережі.

</details>

<details>
<summary>30. Що таке Security Group?</summary>

#### AWS

**Security Group (SG)** — це stateful virtual firewall на рівні ENI/ресурсу
(наприклад EC2, ENI, RDS).

Особливості:

- правила `allow` (deny-правил немає);
- stateful логіка: зворотний трафік дозволяється автоматично;
- правила для inbound і outbound трафіку.

```bash
aws ec2 describe-security-groups --group-ids sg-1234567890abcdef0
aws ec2 authorize-security-group-ingress --group-id sg-1234567890abcdef0 --protocol tcp --port 443 --cidr 10.0.0.0/16
```

**Коротко:**

- SG = основний мережевий контроль доступу до ресурсу.
- Stateful + only allow rules.
- Рекомендовано відкривати лише необхідні порти/джерела.

</details>

<details>
<summary>31. У чому різниця між Security Groups і Network ACL?</summary>

#### AWS

- **Security Group**:
  stateful, працює на рівні ресурсу/ENI, підтримує лише allow-правила.
- **Network ACL (NACL)**:
  stateless, працює на рівні subnet, підтримує allow і deny, правила
  обробляються за номером (ordered rules).

SG зазвичай використовують як primary захист, NACL — як додатковий рівень
контролю на межі subnet.

**Коротко:**

- SG: stateful, resource-level, allow only.
- NACL: stateless, subnet-level, allow/deny.
- Найкраща практика: SG як основний, NACL як додатковий control layer.

</details>

<details>
<summary>32. Що таке VPC Peering?</summary>

#### AWS

**VPC Peering** — це приватне мережеве з'єднання між двома VPC, яке дозволяє
ресурсам обмінюватись трафіком через приватні IP.

Важливі обмеження:

- немає transitive routing;
- CIDR-діапазони VPC не повинні перетинатись;
- маршрути потрібно явно додавати з обох сторін.

**Коротко:**

- Peering напряму з'єднує дві VPC.
- Трафік іде по приватній AWS-мережі.
- Підходить для простих схем "точка-точка".

</details>

<details>
<summary>33. Що таке AWS Transit Gateway?</summary>

#### AWS

**AWS Transit Gateway (TGW)** — це керований мережевий хаб, який централізовано
з'єднує багато VPC і on-prem мережі (через VPN/Direct Connect).

Замість mesh peering-схеми "кожен з кожним" використовується hub-and-spoke
модель, що спрощує масштабування й керування маршрутами.

**Коротко:**

- TGW = централізований роутинг-хаб для багатьох мереж.
- Зменшує складність при великій кількості VPC.
- Підходить для enterprise та multi-account архітектур.

</details>

<details>
<summary>34. Коли варто використовувати VPC Peering, а коли Transit Gateway?</summary>

#### AWS

Загальне правило вибору:

- **VPC Peering**: мало VPC, прості зв'язки, невисока динаміка топології.
- **Transit Gateway**: багато VPC/акаунтів, централізований контроль маршрутизації,
  інтеграція з on-prem, вимоги до масштабованості та керованості.

Peering швидко ускладнюється при зростанні кількості VPC (N^2 connections), тоді
як TGW краще масштабується організаційно й технічно.

**Коротко:**

- Невелика топологія: peering.
- Велика/enterprise топологія: TGW.
- TGW зазвичай кращий для довгострокової мережевої стратегії.

</details>

<details>
<summary>35. Що таке VPC Flow Logs?</summary>

#### AWS

**VPC Flow Logs** — це журнал метаданих мережевого трафіку в VPC на рівні
VPC/subnet/ENI.

Flow Logs не містять payload пакетів, але показують:

- source/destination IP;
- ports/protocol;
- accept/reject;
- обсяг трафіку й часові інтервали.

Логи можна відправляти в CloudWatch Logs або S3 для аналізу, безпеки й
діагностики мережевих проблем.

```bash
aws ec2 create-flow-logs \
  --resource-type VPC \
  --resource-ids vpc-1234567890abcdef0 \
  --traffic-type ALL \
  --log-destination-type cloud-watch-logs \
  --log-group-name /aws/vpc/flowlogs
```

**Коротко:**

- Flow Logs = телеметрія мережевих потоків у VPC.
- Корисні для troubleshooting, audit і security analytics.
- Показують факт і параметри трафіку, але не вміст пакетів.

</details>

<details>
<summary>36. Як усунути проблеми з мережевим підключенням у VPC?</summary>

#### AWS

Практичний чекліст діагностики:

1. Перевірити **route table** (чи є маршрут до потрібної мережі/шлюзу).
2. Перевірити **Security Group** (inbound/outbound правила).
3. Перевірити **NACL** (deny/порядок правил, ephemeral ports).
4. Перевірити наявність/стан **IGW, NAT, TGW, peering**.
5. Переконатися у відсутності **overlapping CIDR** між мережами.
6. Проаналізувати **VPC Flow Logs** (accept/reject і напрямок трафіку).
7. Перевірити DNS резолвінг (Route 53 Resolver, private hosted zones).
8. Використати Reachability Analyzer / packet-level утиліти на інстансах.

Починати краще з найпростішого: SG + route table, бо це найчастіші причини.

```bash
aws ec2 describe-network-interfaces --filters Name=vpc-id,Values=vpc-1234567890abcdef0
aws ec2 describe-network-acls --filters Name=vpc-id,Values=vpc-1234567890abcdef0
aws ec2 search-transit-gateway-routes --transit-gateway-route-table-id tgw-rtb-1234 --filters Name=route-search.exact-match,Values=10.0.2.0/24
```

**Коротко:**

- Troubleshooting VPC = маршрут + фаєрвол + шлюзи + DNS.
- Flow Logs допомагають швидко локалізувати точку відмови.
- Системний чекліст економить час на інцидентах.

</details>

<details>
<summary>37. Що таке AWS Direct Connect і коли його використовують?</summary>

#### AWS

**AWS Direct Connect (DX)** — це виділене приватне мережеве з'єднання між
on-prem дата-центром/офісом і AWS, в обхід публічного інтернету.

Коли використовують:

- стабільні високі обсяги трафіку між on-prem і AWS;
- вимоги до передбачуваної затримки та пропускної здатності;
- підвищені вимоги до безпеки/комплаєнсу;
- гібридні архітектури enterprise-рівня.

Direct Connect часто комбінують із VPN як backup-каналом.

```bash
aws directconnect describe-connections
aws directconnect describe-virtual-interfaces
```

**Коротко:**

- Direct Connect = приватний канал до AWS.
- Дає стабільніше з'єднання, ніж інтернет-VPN.
- Підходить для гібридних і high-throughput сценаріїв.

</details>

<details>
<summary>38. Що таке Amazon EC2?</summary>

#### AWS

**Amazon EC2 (Elastic Compute Cloud)** — це сервіс віртуальних серверів у AWS
для запуску застосунків з гнучким керуванням CPU, RAM, диском, мережею та ОС.

EC2 дає можливість швидко створювати інстанси, масштабувати їх, інтегрувати з
VPC, IAM, EBS, ELB, Auto Scaling та іншими сервісами AWS.

Це базовий IaaS-компонент для сценаріїв, де потрібен контроль над runtime
середовищем і операційною системою.

```bash
aws ec2 run-instances --image-id ami-xxxxxxxx --instance-type t3.micro --count 1
aws ec2 describe-instances --filters Name=instance-state-name,Values=running
```

**Коротко:**

- EC2 = віртуальні сервери в AWS.
- Підходить для широкого спектра workload-ів: web, API, batch, stateful.
- Дає високий контроль, але вимагає операційного менеджменту.

</details>

<details>
<summary>39. Що таке AMI?</summary>

#### AWS

**AMI (Amazon Machine Image)** — це шаблон для запуску EC2-інстансу, який
містить:

- базову ОС;
- preinstalled ПЗ (за потреби);
- конфігурацію запуску (параметри блокових пристроїв тощо).

AMI можуть бути:

- AWS-provided;
- community;
- власні (custom golden images).

В production часто використовують versioned custom AMI для передбачуваних
деплоїв і швидкого масштабування.

**Коротко:**

- AMI = образ інстансу для запуску EC2.
- Стандартизує середовище і прискорює provisioning.
- Краще керувати AMI як версійованим артефактом.

</details>

<details>
<summary>40. Як обрати тип EC2-інстансу?</summary>

#### AWS

Вибір типу інстансу залежить від профілю навантаження:

1. Визначити bottleneck: CPU, RAM, disk IOPS/throughput, network.
2. Обрати сімейство:
   - `t`/`m` — загального призначення;
   - `c` — compute optimized;
   - `r`/`x` — memory optimized;
   - `i`/`d` — storage optimized;
   - `g`/`p`/`inf` — GPU/ML.
3. Перевірити вимоги до архітектури (x86 vs Graviton/ARM).
4. Провести навантажувальні тести та оцінити ціну/продуктивність.
5. Додати права на масштабування (ASG), а не "оверсайзити" один інстанс.

Практика: почати з консервативного розміру, зібрати метрики, оптимізувати на
основі реальних даних.

**Коротко:**

- Тип EC2 обирають за фактичним профілем workload.
- Рішення підтверджують тестами і метриками.
- Краще scale-out + right-sizing, ніж постійний overprovisioning.

</details>

<details>
<summary>41. Які моделі оплати EC2 існують (On-Demand, Reserved, Spot, Savings Plans)?</summary>

#### AWS

Основні моделі ціноутворення EC2:

- **On-Demand**: оплата за фактичне використання без довгих зобов'язань;
  найгнучкіший, але найдорожчий варіант.
- **Reserved Instances (RI)**: зобов'язання на 1 або 3 роки з нижчою ціною;
  підходить для стабільного базового навантаження.
- **Spot Instances**: використання вільної потужності зі значною знижкою;
  інстанс можуть перервати, тому підходить для fault-tolerant задач.
- **Savings Plans**: модель зобов'язання по витратах ($/год) на 1 або 3 роки,
  яка дає знижки з більшою гнучкістю, ніж RI.

Оптимальна стратегія зазвичай гібридна: baseline на RI/Savings Plans, bursts на
On-Demand, batch/асинхронні задачі на Spot.

**Коротко:**

- On-Demand: гнучко, але дорожче.
- RI/Savings Plans: дешевше для стабільного споживання.
- Spot: найдешевше, але з ризиком переривання.

</details>

<details>
<summary>42. Що таке Auto Scaling?</summary>

#### AWS

**Auto Scaling** — це механізм автоматичної зміни кількості ресурсів залежно
від навантаження, метрик або розкладу.

Для EC2 це зазвичай означає автоматичне додавання/видалення інстансів, щоб:

- підтримувати продуктивність під навантаженням;
- зменшувати витрати при спаді трафіку;
- покращувати відмовостійкість через self-healing.

**Коротко:**

- Auto Scaling автоматично підлаштовує capacity.
- Дає баланс між продуктивністю, надійністю та вартістю.
- Ключовий елемент еластичної cloud-архітектури.

</details>

<details>
<summary>43. Що таке Auto Scaling Group (ASG)?</summary>

#### AWS

**Auto Scaling Group (ASG)** — це логічна група EC2-інстансів, яка підтримує
бажану кількість (`desired capacity`) і виконує scaling політики.

ASG оперує параметрами:

- `min`, `desired`, `max` capacity;
- Launch Template/Configuration;
- health checks (EC2/ELB);
- scaling policies (target tracking, step, scheduled).

ASG автоматично замінює нездорові інстанси, що підвищує доступність сервісу.

```bash
aws autoscaling describe-auto-scaling-groups --auto-scaling-group-names app-asg
aws autoscaling set-desired-capacity --auto-scaling-group-name app-asg --desired-capacity 6
```

**Коротко:**

- ASG керує життєвим циклом групи EC2.
- Автоматизує scale in/out і self-healing.
- Основний інструмент для resilient EC2 workload-ів.

</details>

<details>
<summary>44. Що таке Launch Template?</summary>

#### AWS

**Launch Template** — це версійований шаблон конфігурації запуску EC2.

У ньому задають:

- AMI;
- instance type;
- security groups;
- block devices;
- IAM instance profile;
- user data;
- network параметри;
- додаткові опції (наприклад, mixed instances policy в ASG).

Launch Template використовується ASG, EC2 Fleet і Spot Fleet, та вважається
сучасною заміною Launch Configuration.

```bash
aws ec2 create-launch-template \
  --launch-template-name web-lt \
  --launch-template-data '{"ImageId":"ami-xxxxxxxx","InstanceType":"t3.small"}'
aws ec2 describe-launch-template-versions --launch-template-name web-lt
```

**Коротко:**

- Launch Template стандартизує запуск EC2.
- Підтримує версії і повторювані деплої.
- Рекомендований варіант для ASG у production.

</details>

<details>
<summary>45. У чому різниця між зупинкою та видаленням інстансу?</summary>

#### AWS

- **Stop (зупинка)**:
  інстанс вимикається, але залишається у вашому акаунті; EBS root volume
  зберігається (якщо не ephemeral); за compute під час stop ви не платите.
- **Terminate (видалення)**:
  інстанс остаточно видаляється; root volume зазвичай теж видаляється, якщо
  увімкнено `DeleteOnTermination`.

Після terminate інстанс не можна "запустити назад" — потрібен новий запуск з
AMI/шаблону.

**Коротко:**

- Stop = тимчасова зупинка із збереженням інстансу.
- Terminate = остаточне видалення інстансу.
- Перед terminate важливо перевіряти політику збереження даних.

</details>

<details>
<summary>46. Що таке EC2 Placement Groups і коли їх використовують?</summary>

#### AWS

**Placement Group** — це механізм контролю фізичного розміщення EC2-інстансів
для оптимізації latency, throughput або fault isolation.

Типи:

- **Cluster**: щільне розміщення в межах однієї AZ для дуже низької затримки і
  високої пропускної здатності між інстансами.
- **Spread**: рознесення інстансів по різному обладнанню для мінімізації ризику
  одночасного падіння.
- **Partition**: групування по логічних partition-ах з ізоляцією відмов між
  групами (часто для великих distributed систем).

**Коротко:**

- Placement Groups керують фізичною топологією інстансів.
- Використовуються для вимог до мережевої продуктивності або fault isolation.
- Потрібні не завжди, а коли є чітка технічна причина.

</details>

<details>
<summary>47. Що таке Elastic Load Balancing (ELB)?</summary>

#### AWS

**Elastic Load Balancing (ELB)** — це керований сервіс AWS, який автоматично
розподіляє вхідний трафік між кількома цілями (EC2, IP, контейнерами, Lambda)
в одній або кількох Availability Zones.

ELB також виконує health checks і направляє трафік лише на здорові backend-и,
що підвищує стабільність та доступність застосунку.

```bash
aws elbv2 describe-load-balancers
aws elbv2 describe-target-health --target-group-arn arn:aws:elasticloadbalancing:...
```

**Коротко:**

- ELB розподіляє навантаження між інстансами/сервісами.
- Інтегрується з Auto Scaling та health checks.
- Ключовий компонент для high availability в AWS.

</details>

<details>
<summary>48. Які типи балансувальників навантаження існують (ALB, NLB, GWLB)?</summary>

#### AWS

В AWS (ELB family) основні типи:

- **ALB (Application Load Balancer, Layer 7)**:
  HTTP/HTTPS балансування, host/path-based routing, інтеграція з контейнерами,
  підтримка WebSocket і modern web-сценаріїв.
- **NLB (Network Load Balancer, Layer 4)**:
  дуже висока продуктивність і низька затримка для TCP/UDP/TLS трафіку,
  підходить для високонавантажених або протокольно-специфічних сервісів.
- **GWLB (Gateway Load Balancer)**:
  балансування трафіку на мережеві virtual appliances (firewall, IDS/IPS),
  використовується для централізованої network security інспекції.

**Коротко:**

- ALB: L7, "розумний" routing для web/API.
- NLB: L4, максимальна продуктивність і стабільна latency.
- GWLB: балансування для мережевих security appliance-ів.

</details>

<details>
<summary>49. Як балансування навантаження підвищує доступність системи?</summary>

#### AWS

Балансування підвищує доступність через кілька механізмів:

1. Розподіл трафіку між кількома інстансами замість single point of failure.
2. Автоматичне виключення нездорових backend-ів за health checks.
3. Підтримка multi-AZ: трафік продовжує обслуговуватись при падінні окремої AZ.
4. Інтеграція з Auto Scaling: система адаптується до змін навантаження.
5. Плавні деплої (rolling/blue-green) з меншим ризиком downtime.

У результаті ELB зменшує ймовірність повної недоступності та скорочує вплив
часткових відмов.

**Коротко:**

- LB прибирає single point of failure на рівні compute.
- Health checks і multi-AZ підвищують стійкість до відмов.
- Разом з ASG забезпечує еластичність і стабільний SLA.

</details>

<details>
<summary>50. Що таке AWS Lambda?</summary>

#### AWS

**AWS Lambda** — це serverless compute сервіс, який запускає код у відповідь на
події без керування серверами.

Ви завантажуєте функцію, налаштовуєте тригери (API Gateway, S3, SQS, EventBridge
тощо), а AWS автоматично виконує масштабування, availability та частину
операційного менеджменту.

Оплата відбувається за кількість викликів і фактичний час виконання.

```bash
aws lambda list-functions
aws lambda invoke --function-name hello-api /tmp/lambda-response.json
```

**Коротко:**

- Lambda = запуск коду "по події" без адміністрування серверів.
- Автоматично масштабується під навантаження.
- Підходить для event-driven і serverless архітектур.

</details>

<details>
<summary>51. Коли варто використовувати Lambda замість EC2?</summary>

#### AWS

Lambda доцільна, коли:

- навантаження нерівномірне або bursty;
- задачі event-driven і короткоживучі;
- важливі швидкість розробки та мінімальний operations overhead;
- потрібна дрібна оплата за фактичне використання.

EC2 краще, коли:

- потрібен повний контроль над ОС/runtime;
- є довготривалі процеси або специфічні системні залежності;
- критичні стабільні latency-вимоги без cold start ефекту;
- workload постійний і передбачуваний (може бути вигіднішим по ціні).

**Коротко:**

- Lambda: event-driven, короткі задачі, мінімум ops.
- EC2: максимальний контроль і гнучкість середовища.
- Вибір залежить від патерну навантаження і технічних обмежень.

</details>

<details>
<summary>52. Які обмеження має AWS Lambda?</summary>

#### AWS

Типові обмеження Lambda:

- обмежений максимальний час виконання одного invoke;
- ліміти на пам'ять, ephemeral storage та розмір deployment package/image;
- модель stateless execution (локальний стан не гарантований між викликами);
- concurrency ліміти на акаунт/функцію;
- мережеві особливості при роботі у VPC (додаткова складність і latency).

Через ці обмеження Lambda не завжди підходить для довгих або stateful процесів.

**Коротко:**

- Lambda має runtime і resource ліміти.
- Не ідеальна для long-running або stateful workload-ів.
- Потрібно враховувати concurrency та deployment constraints.

</details>

<details>
<summary>53. Що таке cold start?</summary>

#### AWS

**Cold start** — це додаткова затримка під час першого запуску Lambda-функції
(або після періоду неактивності), коли AWS ініціалізує execution environment.

Затримка складається з:

- підняття середовища виконання;
- завантаження коду/залежностей;
- ініціалізації вашого runtime-коду.

При "warm" викликах цей етап зазвичай відсутній або значно менший.

**Коротко:**

- Cold start = стартова затримка першого invoke.
- Найбільш помітний у latency-чутливих API.
- Потрібно враховувати при проєктуванні serverless рішень.

</details>

<details>
<summary>54. Як зменшити затримку cold start?</summary>

#### AWS

Практичні способи:

1. Використовувати **Provisioned Concurrency** для критичних функцій.
2. Зменшувати розмір deployment package та залежностей.
3. Оптимізувати ініціалізацію коду (lazy init, менше "важких" імпортів).
4. Обирати швидший runtime для вашого сценарію.
5. Уникати зайвої VPC-інтеграції, якщо вона не потрібна.
6. Розділяти "важкі" функції на менші спеціалізовані.

Для latency-critical endpoint-ів Provisioned Concurrency зазвичай найефективніший
інструмент.

```bash
aws lambda put-provisioned-concurrency-config \
  --function-name hello-api \
  --qualifier prod \
  --provisioned-concurrent-executions 10
```

**Коротко:**

- Головний важіль: Provisioned Concurrency.
- Менший пакет і легша ініціалізація = швидший старт.
- Архітектурна декомпозиція теж зменшує cold start вплив.

</details>

<details>
<summary>55. Що таке Lambda@Edge?</summary>

#### AWS

**Lambda@Edge** — це запуск Lambda-функцій на edge-локаціях CloudFront для
обробки запитів/відповідей ближче до користувача.

Типові кейси:

- модифікація HTTP headers;
- geo-based логіка та редіректи;
- lightweight аутентифікація/авторизація;
- A/B routing на edge.

Це дозволяє зменшити latency і винести частину логіки з origin.

**Коротко:**

- Lambda@Edge виконує код на рівні CloudFront edge.
- Підходить для request/response трансформацій і edge-логіки.
- Допомагає зменшити затримку для глобальної аудиторії.

</details>

<details>
<summary>56. Як спроєктувати serverless API на AWS?</summary>

#### AWS

Базовий production-патерн:

1. **API Gateway** як зовнішній HTTP вхід (routing, throttling, auth).
2. **Lambda** для бізнес-логіки.
3. **DynamoDB/RDS/Aurora Serverless** для data layer.
4. **SQS/SNS/EventBridge** для асинхронної обробки.
5. **IAM + Cognito/JWT authorizer** для безпеки.
6. **CloudWatch/X-Ray** для логів, метрик і трасування.
7. **IaC (CDK/CloudFormation/Terraform)** для повторюваних деплоїв.

Ключові принципи:

- API має бути stateless;
- ідемпотентність для write-операцій;
- retries + DLQ для асинхронних потоків;
- версіонування API і контроль backward compatibility;
- cost/latency оптимізація на основі метрик.

```bash
aws apigatewayv2 create-api --name app-http-api --protocol-type HTTP
aws lambda create-function --function-name app-handler --runtime nodejs20.x --role arn:aws:iam::123456789012:role/lambda-exec --handler index.handler --zip-file fileb://function.zip
```

**Коротко:**

- Типовий стек: API Gateway + Lambda + managed data store.
- Надійність дають асинхронні патерни, retries і DLQ.
- Без IaC, observability і чіткої auth-моделі serverless API буде крихким.

</details>

<details>
<summary>57. Що таке Amazon S3?</summary>

#### AWS

**Amazon S3 (Simple Storage Service)** — це масштабоване object storage сховище
в AWS для зберігання файлів (objects) у buckets.

S3 використовується для backup, data lake, логів, статичного контенту, архівів
та інтеграцій між сервісами.

Ключові властивості: висока надійність, майже необмежена масштабованість,
інтеграція з IAM/KMS/CloudFront/Analytics сервісами.

```bash
aws s3 mb s3://my-interview-bucket
aws s3 cp ./artifact.zip s3://my-interview-bucket/releases/
```

**Коротко:**

- S3 = кероване object storage в AWS.
- Підходить для великих обсягів неструктурованих даних.
- Базовий сервіс для data, backup і static content сценаріїв.

</details>

<details>
<summary>58. Які класи зберігання існують у S3?</summary>

#### AWS

Основні класи S3:

- **S3 Standard** — частий доступ, низька затримка.
- **S3 Intelligent-Tiering** — автоматичне переміщення між tier-ами за патерном доступу.
- **S3 Standard-IA** — рідший доступ, дешевше зберігання, дорожчий retrieval.
- **S3 One Zone-IA** — як IA, але в одній AZ (нижча вартість, менша resilience).
- **S3 Glacier Instant Retrieval** — архівні дані з мілісекундним доступом.
- **S3 Glacier Flexible Retrieval** — архів із хвилинами/годинами на відновлення.
- **S3 Glacier Deep Archive** — найдешевше довготривале архівування з повільним відновленням.

Вибір класу базується на частоті доступу, вимогах до latency і вартості retrieval.

**Коротко:**

- "Гарячі" дані: Standard/Intelligent-Tiering.
- "Холодні" дані: IA/Glacier.
- Оптимізація вартості = правильний storage class + lifecycle.

</details>

<details>
<summary>59. Що таке versioning у S3?</summary>

#### AWS

**S3 Versioning** — це механізм зберігання кількох версій одного об'єкта в
bucket.

Після увімкнення versioning:

- кожне оновлення створює нову версію;
- випадкове видалення стає recoverable;
- можна відкотитись до попередньої версії.

Це критично для захисту від помилок користувачів і частини сценаріїв ransomware.

```bash
aws s3api put-bucket-versioning --bucket my-interview-bucket --versioning-configuration Status=Enabled
aws s3api list-object-versions --bucket my-interview-bucket --prefix releases/artifact.zip
```

**Коротко:**

- Versioning зберігає історію змін об'єктів.
- Дає можливість відновлення після overwrite/delete.
- Рекомендований для важливих production bucket-ів.

</details>

<details>
<summary>60. Що таке lifecycle policies у S3?</summary>

#### AWS

**S3 Lifecycle policies** — це правила автоматичного керування життєвим циклом
об'єктів.

Вони дозволяють:

- переводити об'єкти між storage classes (наприклад Standard -> IA -> Glacier);
- видаляти старі версії або об'єкти після заданого терміну;
- оптимізувати вартість без ручних операцій.

Lifecycle зазвичай будують на основі retention-вимог і access pattern.

```bash
aws s3api put-bucket-lifecycle-configuration \
  --bucket my-interview-bucket \
  --lifecycle-configuration file://lifecycle.json
```

**Коротко:**

- Lifecycle автоматизує перехід/видалення об'єктів.
- Знижує витрати на зберігання.
- Важливий інструмент для data governance у S3.

</details>

<details>
<summary>61. Що таке S3 Object Lock?</summary>

#### AWS

**S3 Object Lock** забезпечує WORM-поведінку (Write Once Read Many) для об'єктів:
їх не можна змінити або видалити до завершення retention-періоду.

Режими:

- **Governance mode** — видалення/зміна обмежені, але можливі для окремих
  привілейованих ролей.
- **Compliance mode** — жорстке блокування без обходу до закінчення retention.

Застосовується для regulatory/compliance вимог і захисту від навмисного або
випадкового видалення.

**Коротко:**

- Object Lock = незмінність даних на заданий період.
- Підтримує Governance і Compliance режими.
- Ключовий контроль для immutable backup стратегій.

</details>

<details>
<summary>62. Що таке MFA Delete?</summary>

#### AWS

**MFA Delete** — це додатковий захист у versioned S3 bucket, який вимагає MFA
для критичних дій: видалення версій об'єктів або зміни стану versioning.

Це зменшує ризик випадкового/зловмисного видалення даних при компрометації
облікових даних.

На практиці функція використовується рідше через операційні обмеження, але для
критичних bucket-ів може бути виправданою.

**Коротко:**

- MFA Delete додає другий фактор для небезпечних операцій у S3.
- Працює разом із versioning.
- Підсилює захист від destructive дій.

</details>

<details>
<summary>63. Що таке pre-signed URL?</summary>

#### AWS

**Pre-signed URL** — це тимчасове підписане посилання на S3-об'єкт, яке дає
обмежений доступ без надання постійних AWS credential-ів.

Через pre-signed URL можна:

- завантажити об'єкт (GET);
- завантажити об'єкт у bucket (PUT), залежно від підписаної операції.

Безпека залежить від строку дії URL, scope дозволів і контролю розповсюдження.

```bash
aws s3 presign s3://my-interview-bucket/private/report.csv --expires-in 900
```

**Коротко:**

- Pre-signed URL = тимчасовий контрольований доступ до S3.
- Дозволяє безпечно ділитися файлами без IAM-акаунтів.
- Важливо ставити короткий TTL і мінімальні дозволи.

</details>

<details>
<summary>64. Що таке S3 Access Points?</summary>

#### AWS

**S3 Access Points** — це окремі точки доступу до одного bucket із власними
policy та мережевими обмеженнями.

Вони спрощують доступ у великих середовищах, коли різні команди/застосунки
потребують різних правил до спільного bucket.

Access Points особливо корисні в multi-account архітектурах і для fine-grained
керування доступом.

**Коротко:**

- Access Point = окремий "вхід" до bucket з власною політикою.
- Знижує складність великих bucket policy.
- Дає гнучкий і ізольований контроль доступу для різних споживачів.

</details>

<details>
<summary>65. Що таке Cross-Region Replication (CRR)?</summary>

#### AWS

**Cross-Region Replication (CRR)** — це автоматична реплікація S3-об'єктів з
source bucket в одному регіоні до destination bucket в іншому регіоні.

Типові цілі:

- disaster recovery між регіонами;
- зниження latency для глобальних команд/систем;
- виконання вимог data residency та комплаєнсу.

Для CRR потрібні versioning на обох bucket-ах і відповідні IAM/replication rules.

```bash
aws s3api put-bucket-replication \
  --bucket source-bucket \
  --replication-configuration file://replication.json
```

**Коротко:**

- CRR копіює дані між різними AWS Region.
- Підвищує стійкість і readiness до регіональних збоїв.
- Вимагає продуманих replication policy і cost-контролю.

</details>

<details>
<summary>66. Що таке S3 Transfer Acceleration?</summary>

#### AWS

**S3 Transfer Acceleration** пришвидшує завантаження/вивантаження об'єктів у S3
через глобальну edge-мережу AWS.

Клієнт підключається до найближчої edge-локації, а далі трафік іде оптимізованим
шляхом мережею AWS до bucket.

Найбільший ефект зазвичай у сценаріях далекої географії та нестабільних
міжконтинентальних маршрутів.

**Коротко:**

- Transfer Acceleration покращує швидкість передачі в S3 на глобальних дистанціях.
- Працює через edge точки AWS.
- Доцільність потрібно підтверджувати тестами й вартістю.

</details>

<details>
<summary>67. Який максимальний розмір об’єкта в S3 і коли використовується multipart upload?</summary>

#### AWS

Максимальний розмір одного об'єкта в S3 — **5 TB**.

**Multipart upload** використовують, коли:

- об'єкт великий (особливо від сотень MB і більше);
- потрібна надійність передачі через нестабільну мережу;
- важливе паралельне завантаження частин для прискорення.

Multipart дозволяє перезавантажувати лише невдалі частини, а не весь файл.

**Коротко:**

- Максимум S3 object size: 5 TB.
- Multipart upload підвищує швидкість і надійність для великих файлів.
- Стандартний підхід для backup/media/data ingestion потоків.

</details>

<details>
<summary>68. Як усунути помилку AccessDenied у S3?</summary>

#### AWS

Чекліст діагностики `AccessDenied` у S3:

1. Перевірити IAM policy користувача/ролі (`Action`, `Resource`, `Condition`).
2. Перевірити bucket policy (explicit deny, умови по IP/VPC endpoint/MFA).
3. Перевірити Block Public Access налаштування.
4. Перевірити ACL (якщо використовуються) і ownership об'єктів.
5. Перевірити KMS дозволи, якщо об'єкт шифрований SSE-KMS.
6. Перевірити SCP/permission boundaries/session policies в Organizations.
7. Використати CloudTrail та IAM Policy Simulator для pinpoint причини deny.

Найчастіше причина — explicit deny або відсутній дозвіл на пов'язану дію
(наприклад `kms:Decrypt` разом із `s3:GetObject`).

```bash
aws s3api get-bucket-policy-status --bucket my-interview-bucket
aws iam simulate-principal-policy --policy-source-arn arn:aws:iam::123456789012:role/AppRole --action-names s3:GetObject --resource-arns arn:aws:s3:::my-interview-bucket/*
```

**Коротко:**

- `AccessDenied` майже завжди про policy layer (IAM/bucket/SCP/KMS).
- Починати з перевірки explicit deny.
- CloudTrail + Policy Simulator суттєво прискорюють root cause аналіз.

</details>

<details>
<summary>69. Як забезпечити безпеку даних у S3?</summary>

#### AWS

Базові практики безпеки S3:

1. Увімкнути **Block Public Access** на рівні акаунта й bucket.
2. Використовувати **least privilege IAM** і bucket policy без wildcard доступів.
3. Увімкнути **шифрування at rest** (SSE-S3 або SSE-KMS).
4. Примусово використовувати **TLS in transit** (deny для non-HTTPS).
5. Увімкнути **versioning** та, за потреби, **Object Lock/MFA Delete**.
6. Налаштувати **logging/audit** (CloudTrail data events, S3 access logs).
7. Регулярно перевіряти конфігурації через AWS Config/Security Hub.

Для критичних даних бажано додати CRR, immutable backup і чіткі retention policy.

```bash
aws s3api put-public-access-block --bucket my-interview-bucket --public-access-block-configuration BlockPublicAcls=true,IgnorePublicAcls=true,BlockPublicPolicy=true,RestrictPublicBuckets=true
aws s3api put-bucket-encryption --bucket my-interview-bucket --server-side-encryption-configuration file://sse.json
```

**Коротко:**

- Безпека S3 = правильні policy + шифрування + аудит.
- Публічний доступ має бути явним винятком, а не дефолтом.
- Versioning і Object Lock підсилюють захист від втрати/знищення даних.

</details>

<details>
<summary>70. Що таке Amazon EBS?</summary>

#### AWS

**Amazon EBS (Elastic Block Store)** — це блокове сховище для EC2-інстансів.
Воно працює як віртуальний диск, який можна підключати до інстансу для
зберігання ОС, застосунків, баз даних і stateful даних.

EBS підтримує різні типи томів (SSD/HDD), зміну розміру, шифрування, snapshots
та інтеграцію з IAM/KMS/CloudWatch.

**Коротко:**

- EBS = persistent block storage для EC2.
- Підходить для ОС, БД і stateful workload-ів.
- Дає гнучкий контроль продуктивності й резервного копіювання.

</details>

<details>
<summary>71. У чому різниця між EBS і Instance Store?</summary>

#### AWS

- **EBS**:
  мережеве persistent сховище, дані зберігаються після stop/start інстансу,
  підтримує snapshots.
- **Instance Store**:
  локальний диск фізичного хоста з дуже низькою затримкою, але дані еферемерні
  і втрачаються при stop/terminate або збоях хоста.

EBS обирають для важливих даних, Instance Store — для тимчасових кешів, буферів
або високошвидкісних scratch-даних.

**Коротко:**

- EBS: надійне persistent storage.
- Instance Store: швидке, але тимчасове локальне сховище.
- Для критичних даних використовують EBS.

</details>

<details>
<summary>72. Що таке EBS snapshots?</summary>

#### AWS

**EBS Snapshot** — це point-in-time копія EBS-тома, яка зберігається в S3
(керовано AWS) і використовується для backup/restore/DR.

Snapshot-и інкрементальні: після першого повного знімка зберігаються лише зміни,
що оптимізує вартість і час створення.

Зі snapshot можна:

- відновити том;
- створити новий том у тій самій або іншій AZ;
- копіювати між регіонами для DR.

**Коротко:**

- Snapshot = резервна копія EBS на певний момент часу.
- Інкрементальна модель знижує витрати.
- Основний механізм backup і відновлення для EBS.

</details>

<details>
<summary>73. Як автоматизувати резервне копіювання EBS?</summary>

#### AWS

Типові способи автоматизації:

1. **AWS Backup**:
   централізовані backup plans, retention, lifecycle, cross-account/region policy.
2. **Amazon Data Lifecycle Manager (DLM)**:
   автоматичне створення/видалення EBS snapshots за розкладом.
3. **IaC + теги**:
   застосування політик до ресурсів за тегами (`Environment`, `BackupPolicy`).

Для production важливо мати:

- чіткі RPO/RTO;
- регулярні restore-тести;
- контроль retention і витрат.

**Коротко:**

- Найзручніше: AWS Backup або DLM за розкладом.
- Тегування допомагає масштабувати backup-політики.
- Backup без регулярного restore test не гарантує відновлення.

</details>

<details>
<summary>74. Що таке Amazon EFS?</summary>

#### AWS

**Amazon EFS (Elastic File System)** — це кероване мережеве файлове сховище
(NFS), яке можна одночасно монтувати на багато EC2-інстансів.

EFS автоматично масштабується, підтримує multi-AZ доступність і підходить для
спільних файлових даних: web content, shared configs, ML/analytics pipelines.

**Коротко:**

- EFS = кероване shared file storage (NFS) у AWS.
- Одночасний доступ з кількох інстансів.
- Підходить для POSIX-сумісних спільних файлових сценаріїв.

</details>

<details>
<summary>75. Що таке Amazon FSx?</summary>

#### AWS

**Amazon FSx** — це сімейство керованих файлових сервісів AWS для спеціалізованих
workload-ів із конкретними файловими протоколами та вимогами.

Основні варіанти:

- **FSx for Windows File Server** (SMB, AD-інтеграція);
- **FSx for Lustre** (високопродуктивні HPC/ML workload-и);
- **FSx for NetApp ONTAP** (enterprise storage features);
- **FSx for OpenZFS** (POSIX, ZFS можливості).

FSx обирають, коли потрібен конкретний enterprise/HPC файл-сервіс, а не
універсальний NFS-підхід EFS.

**Коротко:**

- FSx = керовані "спеціалізовані" файлові системи AWS.
- Вибір залежить від протоколу, продуктивності й enterprise-функцій.
- Часто використовується для Windows, HPC та storage-heavy систем.

</details>

<details>
<summary>76. У чому різниця між S3, EBS та EFS?</summary>

#### AWS

- **S3** — object storage:
  доступ через API, майже необмежений масштаб, не монтується як класичний диск
  за замовчуванням; ідеально для файлів, backup, data lake, static assets.
- **EBS** — block storage:
  диск для одного EC2 (в межах AZ), низька latency, добре для ОС, БД, stateful
  сервісів на окремому інстансі.
- **EFS** — file storage (NFS):
  спільний доступ для багатьох інстансів, POSIX-сумісність, зручно для shared
  файлових сценаріїв.

Вибір залежить від моделі доступу до даних: object vs block vs shared file.

**Коротко:**

- S3: об'єкти через API.
- EBS: блоковий диск для інстансу.
- EFS: спільна файлова система для кількох інстансів.

</details>

<details>
<summary>77. Що таке Amazon RDS?</summary>

#### AWS

**Amazon RDS (Relational Database Service)** — це керований сервіс реляційних
баз даних у AWS, який автоматизує рутинні операції: provisioning, patching,
backup, failover і моніторинг.

RDS дозволяє зосередитись на схемі даних і запитах, а не на адмініструванні
інфраструктури БД.

```bash
aws rds describe-db-instances
aws rds create-db-instance --db-instance-identifier app-db --engine postgres --db-instance-class db.t3.micro --allocated-storage 20 --master-username app --master-user-password 'ChangeMe123!'
```

**Коротко:**

- RDS = managed реляційна БД в AWS.
- Зменшує операційне навантаження на команду.
- Підходить для більшості OLTP-сценаріїв із SQL.

</details>

<details>
<summary>78. Які бази даних підтримує RDS?</summary>

#### AWS

Amazon RDS підтримує основні реляційні рушії:

- **MySQL**
- **PostgreSQL**
- **MariaDB**
- **Oracle**
- **Microsoft SQL Server**
- **Amazon Aurora** (MySQL/PostgreSQL-сумісна)

Вибір рушія залежить від сумісності застосунку, ліцензування, продуктивності і
операційних вимог.

**Коротко:**

- RDS покриває популярні комерційні й open-source SQL двигуни.
- Aurora — окремий high-performance варіант у межах RDS-екосистеми.
- Рушій обирають під workload і вимоги бізнесу.

</details>

<details>
<summary>79. Що таке Multi-AZ?</summary>

#### AWS

**Multi-AZ** — це режим високої доступності для RDS, коли primary база має
синхронно репліковану standby-інстанцію в іншій Availability Zone.

При збої primary RDS автоматично виконує failover на standby, зменшуючи downtime.
Multi-AZ орієнтований на resilience, а не на масштабування читання.

```bash
aws rds modify-db-instance --db-instance-identifier app-db --multi-az --apply-immediately
aws rds describe-db-instances --db-instance-identifier app-db
```

**Коротко:**

- Multi-AZ підвищує відмовостійкість БД.
- Репліка в іншій AZ синхронізується з primary.
- Головна ціль: HA і швидке відновлення при збоях.

</details>

<details>
<summary>80. Що таке Read Replicas?</summary>

#### AWS

**Read Replica** — це асинхронна read-only копія БД для масштабування читання.

Запити SELECT можна направляти на репліки, зменшуючи навантаження на primary.
Read replicas також застосовують для аналітики, звітності або географічного
наближення читачів.

Через асинхронну реплікацію можливий replication lag.

```bash
aws rds create-db-instance-read-replica \
  --db-instance-identifier app-db-read-1 \
  --source-db-instance-identifier app-db
```

**Коротко:**

- Read Replica масштабує read workload.
- Реплікація зазвичай асинхронна.
- Підходить для read-heavy систем і звітності.

</details>

<details>
<summary>81. У чому різниця між Multi-AZ і Read Replicas?</summary>

#### AWS

- **Multi-AZ**:
  про високу доступність і failover; standby не використовується як звичайний
  read endpoint для масштабування.
- **Read Replicas**:
  про масштабування читання; можуть мати lag і не є повноцінною заміною HA
  механізму Multi-AZ.

У production їх часто комбінують: Multi-AZ для стійкості + Read Replicas для
продуктивності читання.

**Коротко:**

- Multi-AZ = HA/failover.
- Read Replicas = scaling read-запитів.
- Це різні задачі, а не взаємовиключні опції.

</details>

<details>
<summary>82. Що таке Amazon Aurora?</summary>

#### AWS

**Amazon Aurora** — це high-performance керована реляційна БД від AWS,
сумісна з MySQL або PostgreSQL.

Aurora має:

- розділені compute і storage;
- distributed storage з високою відмовостійкістю;
- швидкий failover;
- кращу масштабованість і продуктивність порівняно зі стандартними конфігураціями
  open-source рушіїв у багатьох сценаріях.

```bash
aws rds create-db-cluster \
  --db-cluster-identifier app-aurora \
  --engine aurora-postgresql \
  --master-username app \
  --master-user-password 'ChangeMe123!'
```

**Коротко:**

- Aurora = флагманська managed SQL БД в AWS.
- Поєднує сумісність MySQL/PostgreSQL з enterprise-рівнем продуктивності.
- Часто обирається для критичних production систем.

</details>

<details>
<summary>83. Коли варто використовувати DynamoDB замість RDS?</summary>

#### AWS

DynamoDB доцільний, коли:

- потрібна дуже висока масштабованість і низька latency на великих обсягах;
- модель даних key-value/document добре лягає на access patterns;
- потрібна serverless-модель без адміністрування SQL-рушія;
- очікуються різкі піки навантаження з auto scaling.

RDS/Aurora доцільніші, коли потрібні:

- складні SQL-запити, joins, транзакційна реляційна модель;
- сильні вимоги до класичних relational схем і tooling.

**Коротко:**

- DynamoDB: NoSQL, massive scale, predictable low latency.
- RDS: SQL, relational модель, складні запити.
- Вибір визначається access pattern і типом даних.

</details>

<details>
<summary>84. Що таке DynamoDB Global Tables?</summary>

#### AWS

**DynamoDB Global Tables** — це multi-region active-active реплікація таблиць
DynamoDB.

Дані автоматично реплікуються між вибраними регіонами, що дає:

- низьку затримку для користувачів у різних географіях;
- підвищену стійкість до регіональних збоїв;
- можливість будувати глобальні застосунки з локальним доступом до даних.

Конфлікти змін обробляються за моделлю last writer wins.

```bash
aws dynamodb update-table \
  --table-name Orders \
  --replica-updates '[{"Create":{"RegionName":"eu-west-1"}}]'
```

**Коротко:**

- Global Tables = активна реплікація DynamoDB між регіонами.
- Підходить для global low-latency і DR-стратегій.
- Потрібно враховувати conflict resolution і вартість реплікації.

</details>

<details>
<summary>85. Як працюють snapshots баз даних в AWS?</summary>

#### AWS

Snapshots для БД в AWS — це point-in-time резервні копії стану бази на момент
створення.

Для RDS/Aurora доступні:

- **автоматичні backup-и** (в межах retention window);
- **manual snapshots** (зберігаються до видалення вручну).

Snapshots використовують для:

- відновлення після інцидентів;
- клонування середовищ (dev/test);
- копіювання в інший регіон/акаунт для DR.

Практика: регулярно тестувати restore, бо backup без перевірки відновлення
не гарантує працездатний DR.

```bash
aws rds create-db-snapshot --db-instance-identifier app-db --db-snapshot-identifier app-db-manual-20260303
aws rds restore-db-instance-from-db-snapshot --db-instance-identifier app-db-restore --db-snapshot-identifier app-db-manual-20260303
```

**Коротко:**

- Snapshot = контрольна копія БД на конкретний момент.
- Підтримує відновлення, міграції та DR-сценарії.
- Критично важливо мати регулярні restore-тести.

</details>

<details>
<summary>86. Як моніторити продуктивність бази даних?</summary>

#### AWS

Базовий підхід до моніторингу БД в AWS:

1. **CloudWatch metrics**:
   CPU, memory, storage, IOPS, latency, connections, replica lag.
2. **Enhanced Monitoring / Performance Insights** (для RDS/Aurora):
   детальний аналіз wait events, top SQL, bottleneck-ів.
3. **Логи БД**:
   slow query logs, error logs, audit logs.
4. **Алертинг**:
   порогові й anomaly-based alarms з on-call маршрутизацією.
5. **Capacity review**:
   регулярний аналіз трендів для right-sizing і оптимізації індексів/запитів.

Моніторинг має бути проактивним: не лише "бачити падіння", а попереджати деградацію.

```bash
aws cloudwatch get-metric-statistics \
  --namespace AWS/RDS \
  --metric-name CPUUtilization \
  --dimensions Name=DBInstanceIdentifier,Value=app-db \
  --start-time 2026-03-03T00:00:00Z --end-time 2026-03-03T01:00:00Z \
  --period 300 --statistics Average
```

**Коротко:**

- Поєднуйте метрики, логи й query-level аналіз.
- Performance Insights допомагає швидко знайти root cause.
- Без алертингу та регулярного capacity review моніторинг неповний.

</details>

<details>
<summary>87. Що таке Amazon SQS?</summary>

#### AWS

**Amazon SQS (Simple Queue Service)** — це керований сервіс черг повідомлень
для асинхронної взаємодії між компонентами системи.

SQS допомагає розв'язувати сервіси, вирівнювати піки навантаження і підвищувати
надійність через буферизацію та retry-механізми.

```bash
aws sqs create-queue --queue-name orders-standard
aws sqs send-message --queue-url https://sqs.eu-central-1.amazonaws.com/123456789012/orders-standard --message-body '{"orderId":"123"}'
```

**Коротко:**

- SQS = надійна черга повідомлень у AWS.
- Використовується для асинхронної обробки й decoupling сервісів.
- Зменшує ризик втрати повідомлень при тимчасових збоях споживача.

</details>

<details>
<summary>88. У чому різниця між Standard і FIFO чергами?</summary>

#### AWS

- **Standard Queue**:
  майже необмежена пропускна здатність, at-least-once доставка, порядок
  повідомлень не гарантується.
- **FIFO Queue**:
  гарантує порядок (first-in-first-out) і deduplication, але має нижчу
  пропускну здатність порівняно зі Standard.

Вибір залежить від пріоритету: максимальний throughput чи суворий порядок.

**Коротко:**

- Standard: швидкість і масштаб.
- FIFO: порядок і контроль дублікатів.
- FIFO обирають для бізнес-процесів, де порядок критичний.

</details>

<details>
<summary>89. Що таке Amazon SNS?</summary>

#### AWS

**Amazon SNS (Simple Notification Service)** — це керований pub/sub сервіс для
fan-out розсилки повідомлень багатьом підписникам.

SNS може доставляти повідомлення в різні endpoints: SQS, Lambda, HTTP(S),
email, SMS тощо.

```bash
aws sns create-topic --name order-events
aws sns publish --topic-arn arn:aws:sns:eu-central-1:123456789012:order-events --message '{"event":"OrderCreated"}'
```

**Коротко:**

- SNS = сервіс публікації/підписки.
- Один publisher може повідомляти багато споживачів.
- Корисний для event-driven архітектур і нотифікацій.

</details>

<details>
<summary>90. У чому різниця між SNS і SQS?</summary>

#### AWS

- **SQS** — черга (queue): повідомлення обробляє споживач, зазвичай один потік
  обробки на конкретне повідомлення.
- **SNS** — topic/pub-sub: одне повідомлення може бути доставлене багатьом
  підписникам одночасно (fan-out).

Типовий патерн: SNS topic -> кілька SQS черг для ізоляції різних споживачів.

**Коротко:**

- SQS: буферизована черга для decoupled processing.
- SNS: broadcast подій для багатьох підписників.
- Разом часто дають найгнучкішу event-driven схему.

</details>

<details>
<summary>91. Що таке Amazon ECS?</summary>

#### AWS

**Amazon ECS (Elastic Container Service)** — це керований оркестратор
контейнерів від AWS.

ECS керує запуском, масштабуванням і життєвим циклом контейнерів на:

- EC2 (ви керуєте інстансами),
- або Fargate (serverless режим без керування серверами).

**Коротко:**

- ECS = рідний AWS-сервіс для контейнерної оркестрації.
- Простий в інтеграції з IAM, ALB, CloudWatch, Auto Scaling.
- Добрий вибір для команд, що хочуть менше Kubernetes-складності.

</details>

<details>
<summary>92. Що таке AWS Fargate?</summary>

#### AWS

**AWS Fargate** — це serverless compute для контейнерів (ECS/EKS), де AWS
керує інфраструктурою виконання, а ви керуєте лише контейнером і його ресурсами.

Не потрібно адмініструвати EC2-ноди, patching OS або capacity планування на
рівні серверів.

**Коротко:**

- Fargate прибирає операції з керування контейнерними вузлами.
- Оплата за CPU/RAM під запущені задачі.
- Підходить для швидкого старту і спрощення ops.

</details>

<details>
<summary>93. Що таке Amazon EKS?</summary>

#### AWS

**Amazon EKS (Elastic Kubernetes Service)** — це керований сервіс Kubernetes в
AWS.

EKS спрощує запуск і підтримку Kubernetes control plane, інтегрується з IAM,
VPC, ALB/NLB, CloudWatch та іншими AWS сервісами.

Підходить командам, які стандартизують платформу на Kubernetes або мають
міжхмарні/гібридні вимоги.

**Коротко:**

- EKS = managed Kubernetes від AWS.
- Дає сумісність з екосистемою Kubernetes.
- Зазвичай складніший в операціях, ніж ECS.

</details>

<details>
<summary>94. У чому різниця між ECS і EKS?</summary>

#### AWS

- **ECS**:
  нативний AWS-оркестратор, простіший у старті та операціях в межах AWS.
- **EKS**:
  Kubernetes-стандарт, краща портативність і екосистема CNCF, але вища
  складність керування.

Вибір:

- ECS — коли потрібна швидкість і простота в AWS;
- EKS — коли потрібен Kubernetes-стек, portability або стандарт платформи.

**Коротко:**

- ECS: простіше й швидше для AWS-centric команд.
- EKS: більше гнучкості й стандартності, але дорожче в ops.
- Рішення залежить від skillset команди та platform strategy.

</details>

<details>
<summary>95. Коли варто використовувати Fargate замість EC2?</summary>

#### AWS

Fargate доцільний, коли:

- команда хоче мінімізувати операційний менеджмент інфраструктури;
- workload середнього розміру й не потребує low-level host tuning;
- важливі швидкий запуск і безпечна ізоляція задач;
- навантаження змінне, і зручна granular оплата за runtime ресурси.

EC2 доцільний, коли:

- потрібен глибокий контроль над хостом/мережею/агентами;
- потрібні специфічні instance families, локальні диски, GPU профілі;
- при великих стабільних навантаженнях потрібно максимізувати cost efficiency.

**Коротко:**

- Fargate: менше ops, швидше delivery.
- EC2: більше контролю і потенційно краща ціна на великих стабільних обсягах.
- Вибір роблять за trade-off між простотою і контролем.

</details>

<details>
<summary>96. Що таке Amazon CloudWatch?</summary>

#### AWS

**Amazon CloudWatch** — це платформа observability в AWS для збору метрик,
логів, подій і побудови алертингу/дашбордів.

CloudWatch допомагає бачити стан інфраструктури, виявляти деградації та
автоматизувати реакції на інциденти.

```bash
aws cloudwatch list-metrics --namespace AWS/EC2
aws logs tail /aws/lambda/hello-api --since 1h
```

**Коротко:**

- CloudWatch = моніторинг і observability сервіс AWS.
- Об'єднує метрики, логи, алерти та автоматизацію реакцій.
- Базовий інструмент для операційної надійності в AWS.

</details>

<details>
<summary>97. Що таке метрики, логи та alarms у CloudWatch?</summary>

#### AWS

- **Метрики (Metrics)**:
  числові часові ряди (CPUUtilization, latency, errors), що показують стан і
  продуктивність.
- **Логи (Logs)**:
  текстові записи подій/помилок із сервісів і застосунків (CloudWatch Logs).
- **Alarms**:
  правила, які спрацьовують при виході метрик за пороги або за anomaly detection,
  і запускають дії (SNS, Auto Scaling, Incident workflows).

Разом вони дають повний контур виявлення і реагування.

**Коротко:**

- Metrics відповідають на "наскільки добре працює".
- Logs відповідають на "що саме сталося".
- Alarms автоматизують реакцію на відхилення.

</details>

<details>
<summary>98. Що таке AWS CloudTrail?</summary>

#### AWS

**AWS CloudTrail** — це сервіс аудиту API-активності в AWS.

Він записує хто, коли, звідки і яку дію виконав у вашому акаунті (management і,
за потреби, data events), що критично для security, compliance і розслідування
інцидентів.

```bash
aws cloudtrail lookup-events --max-results 20
aws cloudtrail describe-trails
```

**Коротко:**

- CloudTrail = журнал дій і змін у AWS через API.
- Основа audit trail і forensic аналізу.
- Важливий для контролю доступу та відповідності політикам.

</details>

<details>
<summary>99. У чому різниця між CloudWatch і CloudTrail?</summary>

#### AWS

- **CloudWatch**:
  сервіс моніторингу продуктивності й стану (метрики, логи, алерти).
- **CloudTrail**:
  сервіс аудиту керуючих дій/API викликів (хто і що змінив).

CloudWatch більше про operational visibility, CloudTrail — про governance,
security audit і accountability.

**Коротко:**

- CloudWatch: "як працює система".
- CloudTrail: "хто що зробив у системі".
- Обидва сервіси потрібні одночасно в production.

</details>

<details>
<summary>100. Що таке AWS Config?</summary>

#### AWS

**AWS Config** — це сервіс інвентаризації ресурсів і контролю відповідності
конфігурацій політикам.

Він зберігає історію змін конфігурацій, дозволяє оцінювати ресурси через rules
та виявляти drift/невідповідності (наприклад, "S3 bucket має бути encrypted").

```bash
aws configservice describe-configuration-recorders
aws configservice get-compliance-summary-by-config-rule
```

**Коротко:**

- AWS Config відстежує конфігурації ресурсів у часі.
- Допомагає автоматизувати compliance checks.
- Корисний для governance, audit і continuous compliance.

</details>

<details>
<summary>101. Як організувати моніторинг ресурсів AWS?</summary>

#### AWS

Практичний baseline:

1. Збирати **системні метрики** в CloudWatch (compute, storage, network, DB).
2. Централізувати **application logs** і структурувати їх.
3. Налаштувати **аларми** за SLO/SLI і бізнес-критичними порогами.
4. Використовувати **CloudTrail** для audit/security подій.
5. Використовувати **AWS Config** для контролю конфігурацій і drift detection.
6. Додати dashboard-и й on-call процедури з чіткими runbook-ами.
7. Регулярно проводити review алертів (шум/корисність) і capacity трендів.

Моніторинг має покривати не лише інфраструктуру, а й бізнесові KPI та user-facing
latency/error rate.

```bash
aws cloudwatch put-metric-alarm \
  --alarm-name high-5xx \
  --namespace AWS/ApplicationELB \
  --metric-name HTTPCode_ELB_5XX_Count \
  --statistic Sum --period 60 --evaluation-periods 5 --threshold 10 \
  --comparison-operator GreaterThanThreshold \
  --dimensions Name=LoadBalancer,Value=app/my-alb/1234 \
  --alarm-actions arn:aws:sns:eu-central-1:123456789012:oncall
```

**Коротко:**

- Ефективний моніторинг = метрики + логи + аудит + compliance.
- Алерти повинні бути прив'язані до SLO, а не до випадкових порогів.
- Без runbook і on-call процесу моніторинг не доведений до операційної цінності.

</details>

<details>
<summary>102. Що таке AWS CodePipeline?</summary>

#### AWS

**AWS CodePipeline** — це керований сервіс оркестрації CI/CD, який автоматизує
етапи доставки змін: source -> build -> test -> deploy.

Pipeline інтегрується з Git-провайдерами, CodeBuild, CodeDeploy, ECS/EKS,
CloudFormation та іншими інструментами.

```bash
aws codepipeline list-pipelines
aws codepipeline start-pipeline-execution --name app-pipeline
```

**Коротко:**

- CodePipeline керує послідовністю етапів релізу.
- Дає repeatable delivery process і контроль змін.
- Зменшує ручні операції в release management.

</details>

<details>
<summary>103. Що таке AWS CodeBuild?</summary>

#### AWS

**AWS CodeBuild** — це керований сервіс збірки й тестування коду.

Він запускає build jobs у ізольованих середовищах, масштабується автоматично і
може збирати артефакти (наприклад Docker image, binaries, test reports).

```bash
aws codebuild list-projects
aws codebuild start-build --project-name app-build
```

**Коротко:**

- CodeBuild виконує build/test етапи в CI.
- Не потребує окремого керування build-серверами.
- Добре інтегрується з CodePipeline та ECR.

</details>

<details>
<summary>104. Що таке AWS CodeDeploy?</summary>

#### AWS

**AWS CodeDeploy** — це сервіс автоматизованого деплою застосунків на EC2,
on-prem інстанси, Lambda та ECS (через відповідні сценарії).

Підтримує стратегії деплою (rolling, blue/green) і автоматичний rollback при
невдалих релізах.

```bash
aws deploy list-applications
aws deploy create-deployment --application-name app --deployment-group-name prod-dg --revision revisionType=S3,s3Location={bucket=my-artifacts,key=app.zip,bundleType=zip}
```

**Коротко:**

- CodeDeploy автоматизує rollout і rollback.
- Знижує ризики ручного деплою.
- Підтримує безпечні стратегії оновлення.

</details>

<details>
<summary>105. Як спроєктувати CI/CD-пайплайн для контейнерного застосунку?</summary>

#### AWS

Базовий production-патерн:

1. **Source stage**: Git push / PR trigger.
2. **Build stage (CodeBuild)**:
   тести, lint, security scan, збірка Docker image.
3. **Artifact stage**:
   push image в **Amazon ECR** з immutable tag policy.
4. **Deploy stage**:
   ECS/EKS deployment через CodeDeploy/Argo/Helm/IaC.
5. **Verification stage**:
   smoke/integration checks, health gates.
6. **Rollback policy**:
   автоматичний відкат за метриками/алертами.

Обов'язково: secrets management, least privilege IAM, environment parity,
promotion dev -> stage -> prod.

```bash
aws ecr create-repository --repository-name app
aws ecr get-login-password | docker login --username AWS --password-stdin 123456789012.dkr.ecr.eu-central-1.amazonaws.com
docker build -t app:$(git rev-parse --short HEAD) .
docker tag app:$(git rev-parse --short HEAD) 123456789012.dkr.ecr.eu-central-1.amazonaws.com/app:$(git rev-parse --short HEAD)
docker push 123456789012.dkr.ecr.eu-central-1.amazonaws.com/app:$(git rev-parse --short HEAD)
```

**Коротко:**

- Контейнерний CI/CD = build/scan/push/deploy/verify/rollback.
- ECR + автоматичні тести і security gates є must-have.
- Надійність пайплайну визначається контрольними перевірками перед продом.

</details>

<details>
<summary>106. Що таке blue-green deployment?</summary>

#### AWS

**Blue-green deployment** — це стратегія релізу, де є два оточення:

- **Blue**: поточна production-версія;
- **Green**: нова версія.

Після перевірки трафік переключають з Blue на Green. Якщо є проблема —
переключення назад виконується швидко.

**Коротко:**

- Blue/Green мінімізує downtime і ризик релізу.
- Дозволяє швидкий rollback через traffic switch.
- Підходить для критичних production оновлень.

</details>

<details>
<summary>107. Що таке Amazon Athena?</summary>

#### AWS

**Amazon Athena** — це serverless SQL query сервіс для аналізу даних у S3 без
підняття окремого кластера.

Athena використовує schema-on-read підхід і добре підходить для ad-hoc аналітики,
логів та BI-запитів.

```bash
aws athena start-query-execution \
  --query-string "SELECT count(*) FROM logs_2026 WHERE level='ERROR'" \
  --query-execution-context Database=analytics \
  --result-configuration OutputLocation=s3://athena-results-bucket/
```

**Коротко:**

- Athena = SQL по даних у S3.
- Не потребує керування інфраструктурою.
- Ефективна для швидкої аналітики data lake даних.

</details>

<details>
<summary>108. Що таке Amazon Redshift?</summary>

#### AWS

**Amazon Redshift** — це керований data warehouse сервіс для аналітики великих
обсягів структурованих даних (OLAP).

Оптимізований для складних аналітичних запитів, BI-звітності та інтеграції з
ETL/ELT процесами.

```bash
aws redshift describe-clusters
aws redshift-data execute-statement --cluster-identifier analytics-rs --database analytics --db-user admin --sql "SELECT current_date;"
```

**Коротко:**

- Redshift = аналітичне сховище даних (DWH) у AWS.
- Підходить для складних SQL-запитів на великих датасетах.
- Часто використовується як ядро BI-платформи.

</details>

<details>
<summary>109. Що таке Amazon EMR?</summary>

#### AWS

**Amazon EMR (Elastic MapReduce)** — це керований сервіс для запуску
big data фреймворків (Spark, Hadoop, Hive, Presto та ін.) на масштабованому
кластері.

EMR обирають для batch обробки, складних трансформацій і ML pipeline-ів, де
потрібен контроль над обчислювальним кластером.

**Коротко:**

- EMR = керований big data кластерний сервіс.
- Підходить для Spark/Hadoop workload-ів.
- Дає гнучкість і масштаб для data engineering задач.

</details>

<details>
<summary>110. Як побудувати data lake на AWS?</summary>

#### AWS

Базовий підхід:

1. **S3** як центральне сховище (raw/processed/curated зони).
2. **Glue Data Catalog** для централізованих метаданих.
3. **Glue/EMR/Lambda** для ingestion і трансформацій.
4. **Athena/Redshift Spectrum** для SQL-аналітики.
5. **Lake Formation + IAM + KMS** для безпеки і governance.
6. **Data quality + partitioning + формат Parquet/ORC** для продуктивності.

Архітектура має включати lifecycle, versioning, audit і cost-контроль.

```bash
aws s3 mb s3://company-data-lake-raw
aws glue create-database --database-input Name=datalake_raw
aws lakeformation register-resource --resource-arn arn:aws:s3:::company-data-lake-raw
```

**Коротко:**

- Data lake на AWS зазвичай будується навколо S3.
- Catalog, governance і access control не менш важливі, ніж зберігання.
- Продуктивність сильно залежить від формату даних і партиціювання.

</details>

<details>
<summary>111. Що таке AWS Glue і Glue Data Catalog?</summary>

#### AWS

**AWS Glue** — це керований ETL/ELT сервіс для підготовки й трансформації даних.

**Glue Data Catalog** — централізований каталог метаданих таблиць/схем, який
використовують Athena, EMR, Redshift Spectrum та інші аналітичні сервіси.

```bash
aws glue create-crawler --name raw-events-crawler --role AWSGlueServiceRole --database-name datalake_raw --targets S3Targets=[{Path=s3://company-data-lake-raw/events/}]
aws glue start-crawler --name raw-events-crawler
```

**Коротко:**

- Glue виконує data integration і трансформації.
- Data Catalog зберігає схеми й метадані для запитів.
- Разом формують основу керованої data platform на AWS.

</details>

<details>
<summary>112. Що таке AWS Lake Formation?</summary>

#### AWS

**AWS Lake Formation** — сервіс для централізованого керування доступом і
governance у data lake на S3.

Він спрощує налаштування fine-grained permissions (table/column/row), аудит і
data sharing для аналітичних сервісів.

**Коротко:**

- Lake Formation централізує безпеку та governance data lake.
- Дає granular контроль доступу до даних.
- Зменшує складність ручного керування політиками в великих платформах.

</details>

<details>
<summary>113. Що таке Amazon QuickSight?</summary>

#### AWS

**Amazon QuickSight** — це BI-сервіс AWS для побудови дашбордів, візуалізацій і
аналітичних звітів.

Підключається до різних джерел (Redshift, Athena, RDS, S3 тощо) і дозволяє
публікувати інтерактивні бізнес-звіти для команд.

**Коротко:**

- QuickSight = керований BI інструмент AWS.
- Дозволяє створювати дашборди без окремої BI інфраструктури.
- Підходить для self-service аналітики.

</details>

<details>
<summary>114. Як спроєктувати високодоступну архітектуру в AWS?</summary>

#### AWS

Ключові принципи HA:

1. Розподіл компонентів мінімум по двох AZ.
2. Відсутність single points of failure.
3. Використання managed сервісів з вбудованим failover.
4. Auto Scaling + load balancing для compute layer.
5. Декомпозиція на незалежні fault domains.
6. Регулярне тестування сценаріїв відмов (game days).

Ціль — не "уникнути відмов", а зробити систему стійкою до них.

**Коротко:**

- HA в AWS = multi-AZ + self-healing + failover.
- Архітектура має витримувати часткові збої без повного outage.
- Практичне тестування відмов так само важливе, як дизайн.

</details>

<details>
<summary>115. Як реалізувати multi-AZ архітектуру?</summary>

#### AWS

Базовий шаблон:

- ALB/NLB розподіляє трафік по інстансах у 2+ AZ.
- ASG охоплює кілька AZ і автоматично відновлює інстанси.
- БД у Multi-AZ режимі (RDS/Aurora).
- Стан/сесії виносяться в shared layer (ElastiCache/DynamoDB/RDS), а не локально.
- Route tables, SG, NACL і NAT конфігуруються симетрично між AZ.

Multi-AZ потрібно закладати на етапі дизайну, а не "додавати потім".

**Коротко:**

- Multi-AZ = дублювання критичних компонентів між зонами.
- Stateless app layer + stateful HA data layer.
- Симетрична мережева і безпекова конфігурація є обов'язковою.

</details>

<details>
<summary>116. Як спроєктувати глобально розподілену систему?</summary>

#### AWS

Практичні кроки:

1. Визначити активні регіони за latency/compliance вимогами.
2. Використати глобальний routing (Route 53, Global Accelerator, CloudFront).
3. Реалізувати multi-region data strategy (active-active або active-passive).
4. Налаштувати асинхронну/синхронну реплікацію залежно від RPO/RTO.
5. Проєктувати сервіси на eventual consistency і idempotency.
6. Мати runbooks для regional failover/failback.

Глобальна архітектура завжди компроміс між latency, consistency, складністю і
вартістю.

**Коротко:**

- Global architecture = multi-region + smart traffic routing.
- Data replication стратегія є центральним рішенням дизайну.
- Потрібні автоматизація failover і чіткі операційні процедури.

</details>

<details>
<summary>117. Як побудувати архітектуру для обробки даних у реальному часі (IoT / streaming)?</summary>

#### AWS

Типовий real-time патерн:

- Ingestion: IoT Core / Kinesis Data Streams / MSK.
- Stream processing: Lambda / Kinesis Data Analytics / Flink on EMR.
- Storage: S3 (data lake), DynamoDB/ElastiCache для low-latency lookup.
- Serving/analytics: OpenSearch/Redshift/Athena/QuickSight.
- Monitoring: CloudWatch + алертинг по lag, throughput, error rate.

Критичні аспекти: backpressure, retries, idempotency, schema evolution,
dead-letter потоки і data retention.

**Коротко:**

- Real-time pipeline = ingestion -> processing -> storage -> serving.
- Надійність визначають механізми обробки збоїв і повторів.
- Архітектуру треба проєктувати під пікові навантаження й lag-контроль.

</details>

<details>
<summary>118. Які існують стратегії аварійного відновлення?</summary>

#### AWS

Класичні DR-стратегії (від дешевшої до дорожчої):

1. **Backup & Restore** — відновлення з резервних копій.
2. **Pilot Light** — мінімальна "ядрова" інфраструктура постійно активна.
3. **Warm Standby** — зменшена, але працездатна копія середовища.
4. **Multi-Site Active/Active** — повноцінно активні кілька майданчиків.

Кожна стратегія має свій компроміс між RTO/RPO, складністю та вартістю.

**Коротко:**

- DR-стратегії відрізняються швидкістю відновлення і ціною.
- Чим менший RTO/RPO, тим дорожча й складніша реалізація.
- Вибір повинен базуватися на бізнес-критичності сервісу.

</details>

<details>
<summary>119. Як обрати DR-стратегію відповідно до RTO/RPO?</summary>

#### AWS

Алгоритм вибору:

1. Класифікувати сервіси за критичністю.
2. Для кожного визначити цільові **RTO** (час відновлення) і **RPO** (допустима
   втрата даних).
3. Співставити цілі з DR-моделлю:
   - високий RTO/RPO -> backup/restore;
   - середні -> pilot light / warm standby;
   - дуже низькі -> active-active.
4. Перевірити бюджет і операційну готовність.
5. Регулярно тестувати DR-план і коригувати архітектуру.

**Коротко:**

- RTO/RPO — головні вхідні параметри DR-дизайну.
- Немає "універсально найкращої" DR-стратегії.
- DR-план без регулярних тестів не вважається надійним.

</details>

<details>
<summary>120. Як мігрувати велику on-premise базу даних до AWS з мінімальним простоєм?</summary>

#### AWS

Практичний підхід:

1. Виконати assessment (обсяг, schema, dependencies, downtime constraints).
2. Підготувати target БД в AWS (RDS/Aurora/self-managed).
3. Зробити початкове завантаження даних (full load).
4. Налаштувати CDC (Change Data Capture) через AWS DMS або інший інструмент.
5. Прогнати валідацію даних і performance tests.
6. Виконати cutover у вікно мінімального навантаження.
7. Мати rollback plan і чітку комунікацію зі стейкхолдерами.

Ключ для мінімального простою — поетапна міграція з безперервною реплікацією змін.

```bash
aws dms create-replication-instance --replication-instance-identifier mig-ri --replication-instance-class dms.t3.medium --allocated-storage 100
aws dms create-replication-task --replication-task-identifier db-migration-task --source-endpoint-arn arn:aws:dms:...:endpoint:src --target-endpoint-arn arn:aws:dms:...:endpoint:dst --replication-instance-arn arn:aws:dms:...:rep:mig-ri --migration-type full-load-and-cdc --table-mappings file://table-mappings.json
```

**Коротко:**

- Великі БД мігрують через full load + CDC + контрольований cutover.
- DMS часто є базовим інструментом міграції в AWS.
- Успіх визначається rehearsal, валідацією і готовим rollback.

</details>

<details>
<summary>121. Як діагностувати помилки 502 на Application Load Balancer?</summary>

#### AWS

Чекліст для `502` на ALB:

1. Перевірити health status target group.
2. Перевірити, чи backend слухає правильний port/protocol.
3. Перевірити timeout-и ALB і backend застосунку.
4. Перевірити TLS handshake/сертифікати (якщо HTTPS до target).
5. Переглянути ALB access logs і application logs.
6. Перевірити SG/NACL/routes між ALB і targets.
7. Переконатися, що backend повертає валідну HTTP-відповідь.

Часті причини: падіння backend, неправильний health check path/port, timeout
або protocol mismatch.

```bash
aws elbv2 describe-target-health --target-group-arn arn:aws:elasticloadbalancing:...
aws logs tail /aws/elasticloadbalancing/app/my-alb --since 10m
```

**Коротко:**

- `502` означає, що ALB не отримав коректну відповідь від target.
- Діагностика: target health + мережа + таймаути + логи.
- Найшвидший шлях — кореляція ALB logs і логів застосунку.

</details>

<details>
<summary>122. Як усунути таймаути Lambda при підключенні до RDS у VPC?</summary>

#### AWS

Типові причини і дії:

1. Перевірити SG правила між Lambda ENI і RDS.
2. Перевірити route/NACL у subnet-ах Lambda і RDS.
3. Переконатися, що Lambda має доступ до Secrets Manager/KMS (за потреби через VPC endpoints/NAT).
4. Перевірити connection management:
   використати RDS Proxy або пулінг, уникати "нове з'єднання на кожний invoke".
5. Налаштувати адекватні timeout-и Lambda і DB-клієнта.
6. Перевірити ліміти max connections на БД.

Найпоширеніша проблема в serverless + RDS — connection storm.

```bash
aws lambda get-function-configuration --function-name app-handler
aws rds describe-db-proxies
aws ec2 describe-network-interfaces --filters Name=description,Values="AWS Lambda VPC ENI*"
```

**Коротко:**

- Таймаути часто викликані мережею або керуванням DB-з'єднаннями.
- RDS Proxy значно покращує стабільність для Lambda workload-ів.
- Потрібен контроль SG/NACL/routes і connection limits.

</details>

<details>
<summary>123. Як діагностувати проблеми із затримками всередині VPC?</summary>

#### AWS

Практичний план:

1. Визначити сегмент шляху з латентністю (client -> LB -> app -> DB).
2. Перевірити CloudWatch метрики (network, CPU steal/wait, queue depths).
3. Аналізувати VPC Flow Logs для reject/anomaly патернів.
4. Перевірити route tables, NACL, SG на асиметрії.
5. Перевірити DNS latency (Route 53 Resolver, кешування).
6. Оцінити межзонний/міжрегіональний трафік і його вплив.
7. Провести packet/path діагностику з інстансів (mtr/traceroute/tcp checks).

Затримка часто має комбіновану причину: мережа + перевантажений backend.

```bash
aws ec2 describe-network-acls --filters Name=vpc-id,Values=vpc-1234567890abcdef0
aws ec2 describe-flow-logs --filter Name=resource-id,Values=vpc-1234567890abcdef0
aws cloudwatch get-metric-data --metric-data-queries file://latency-queries.json --start-time 2026-03-03T00:00:00Z --end-time 2026-03-03T01:00:00Z
```

**Коротко:**

- Latency troubleshooting починається з чіткої локалізації вузького місця.
- Потрібно дивитися і мережу, і стан обчислювальних компонентів.
- Flow Logs + метрики + прикладні логи дають повну картину.

</details>

<details>
<summary>124. Як проаналізувати раптове зростання витрат в AWS?</summary>

#### AWS

Чекліст аналізу cost spike:

1. В Cost Explorer знайти сервіс, регіон, акаунт, usage type, tag джерела росту.
2. Перевірити аномалії через AWS Cost Anomaly Detection.
3. Зіставити з недавніми змінами (deploy, autoscaling, data transfer, DR tests).
4. Перевірити неочікуваний ріст зберігання, трафіку, запитів, NAT egress.
5. Валідувати RI/Savings Plans coverage і utilization.
6. Побудувати remediation план і бюджетні guardrails.

Важливо відрізняти разову аномалію від нового сталого рівня споживання.

```bash
aws ce get-cost-and-usage \
  --time-period Start=2026-03-01,End=2026-03-04 \
  --granularity DAILY \
  --metrics UnblendedCost \
  --group-by Type=DIMENSION,Key=SERVICE
```

**Коротко:**

- Спершу визначають "хто/де/за що" згенерував витрати.
- Cost Explorer + Anomaly Detection — базові інструменти root cause.
- Після аналізу потрібні технічні і фінансові guardrails.

</details>

<details>
<summary>125. Які інструменти використовуються для оптимізації витрат?</summary>

#### AWS

Основні AWS FinOps інструменти:

- **AWS Cost Explorer** — аналіз витрат і трендів.
- **AWS Budgets** — бюджети та алерти.
- **Cost Anomaly Detection** — виявлення аномалій витрат.
- **AWS Compute Optimizer** — рекомендації з right-sizing.
- **Savings Plans / RI recommendations** — зниження compute cost.
- **Trusted Advisor** — best-practice перевірки (в т.ч. cost).
- **CUR (Cost and Usage Report)** — детальна cost-аналітика.

```bash
aws ce get-dimension-values --time-period Start=2026-03-01,End=2026-03-31 --dimension SERVICE
aws ce get-savings-plans-coverage --time-period Start=2026-03-01,End=2026-03-31 --granularity MONTHLY
```

**Коротко:**

- Оптимізація витрат вимагає і технічних, і фінансових інструментів.
- CUR + Cost Explorer дають глибоку видимість.
- Budgets/Anomaly Detection потрібні для проактивного контролю.

</details>

<details>
<summary>126. Як оптимізувати витрати AWS у production-середовищі?</summary>

#### AWS

Практичні напрями оптимізації:

1. Right-size compute і БД за фактичними метриками.
2. Використовувати Savings Plans/RI для стабільного навантаження.
3. Автоматизувати start/stop non-prod середовищ.
4. Оптимізувати storage classes, lifecycle і data retention.
5. Мінімізувати зайвий data transfer (особливо inter-AZ/inter-region/NAT).
6. Використовувати Spot для fault-tolerant batch/workers.
7. Запровадити тегування і ownership по всіх витратних ресурсах.
8. Вбудувати FinOps review в регулярний операційний цикл.

Оптимізація витрат — це безперервний процес, а не одноразова задача.

```bash
aws compute-optimizer get-ec2-instance-recommendations
aws budgets describe-budgets --account-id 123456789012
```

**Коротко:**

- Cost optimization = архітектурні рішення + операційна дисципліна.
- Найбільший ефект дають right-sizing, commitments і storage hygiene.
- Без тегування та регулярного review витрати швидко виходять з-під контролю.

</details>
