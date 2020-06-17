# Настройка Amazon S3<a name="SigningUpforS3"></a>

Когда вы регистрируетесь в AWS, ваша учетная запись AWS автоматически подписывается на все сервисы AWS, включая Amazon S3\. Но счета выставляются только за те ресурсы, которые вы используете\.

С Amazon S3 вы платите только за то, что использовали\. Для получения более подробной информации о функциях и расценках на Amazon S3, смотрите [страницу Amazon S3](http://aws.amazon.com/s3)\. Если вы новый пользователь Amazon S3, вы можете начать пользоваться Amazon S3 совершенно бесплатно\. Для получения дополнительной информации, смотрите [Бесплатный уровень AWS](http://aws.amazon.com/free)\.

Следуйте этим шагам, чтобы начать работу с Amazon S3:

**Темы**
+ [Зарегистрируйтесь в AWS](#sign-up-for-aws-gsg)
+ [Создайте пользователя IAM](#create-an-iam-user-gsg)
+ [Зайдите под именем пользователя IAM](#signing-in-iam-user-gsg)

## Зарегистрируйтесь в AWS<a name="sign-up-for-aws-gsg"></a>

Если у вас нет учетной записи AWS, создайте ее, путем выполнения следующих шагов\.

**Для регистрации учетной записи AWS**

1. Откройте страницу [https://portal\.aws\.amazon\.com/billing/signup](https://portal.aws.amazon.com/billing/signup)\.

1. Следуйте инструкциям\.

   Часть процедуры регистрации включает в себя получение телефонного звонка и ввод кода подтверждения на клавиатуре телефона\.

AWS пришлет вам электронное письмо с подтверждением по окончании процесса регистрации\. В любой момент вы можете посмотреть состояние вашей учетной записи или управлять вашей учетной записью путем перехода по ссылке [https://aws\.amazon\.com/](https://aws.amazon.com/) и нажатия **My Account**\.

## Создайте пользователя IAM<a name="create-an-iam-user-gsg"></a>

Когда вы впервые создаете учетную запись Amazon Web Services \(AWS\), вы начинаете работу с единой учетной записью\. Эта учетная запись имеет полный доступ ко всем ресурсам и сервисам AWS в пределах вашего аккаунта\. Эта учетная запись AWS называется *root user*\. Когда вы заходите - введите адрес электронной почты и пароль, которые вы использовали при создании учетной записи\.

**Важно**  
Мы настоятельно рекомендуем вам не использовать пользователя root для выполнения повседневных задач, даже административных.\. Вместо этого, придерживайтесь [лучшей практики по использованию корневого(root) пользователя единожды, только для создания вашего первого пользователя IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#create-iam-users)\. Затем надежно спрячьте учетные данные пользователя root и используйте их для выполнения редких задач управления учетными записями и службами\. Чтобы ознакомиться со списком задач, которые могут потребовать использование корневого пользователя, смотрите список [Задач AWS, которые требуют использования корневого пользователя](https://docs.aws.amazon.com/general/latest/gr/aws_tasks-that-require-root.html)\.

Если вы уже зарегистрировались в AWS, но еще не создали для себя пользователя IAM, следуйте этим шагам\.

**To create an administrator user for yourself and add the user to an administrators group \(console\)**

1. Use your AWS account email address and password to sign in as the *[AWS account root user](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html)* to the IAM console at [https://console\.aws\.amazon\.com/iam/](https://console.aws.amazon.com/iam/)\.
**Note**  
We strongly recommend that you adhere to the best practice of using the **Administrator** IAM user below and securely lock away the root user credentials\. Sign in as the root user only to perform a few [account and service management tasks](https://docs.aws.amazon.com/general/latest/gr/aws_tasks-that-require-root.html)\.

1. In the navigation pane, choose **Users** and then choose **Add user**\.

1. For **User name**, enter **Administrator**\.

1. Select the check box next to **AWS Management Console access**\. Then select **Custom password**, and then enter your new password in the text box\.

1. \(Optional\) By default, AWS requires the new user to create a new password when first signing in\. You can clear the check box next to **User must create a new password at next sign\-in** to allow the new user to reset their password after they sign in\.

1. Choose **Next: Permissions**\.

1. Under **Set permissions**, choose **Add user to group**\.

1. Choose **Create group**\.

1. In the **Create group** dialog box, for **Group name** enter **Administrators**\.

1. Choose **Filter policies**, and then select **AWS managed \-job function** to filter the table contents\.

1. In the policy list, select the check box for **AdministratorAccess**\. Then choose **Create group**\.
**Note**  
You must activate IAM user and role access to Billing before you can use the `AdministratorAccess` permissions to access the AWS Billing and Cost Management console\. To do this, follow the instructions in [step 1 of the tutorial about delegating access to the billing console](https://docs.aws.amazon.com/IAM/latest/UserGuide/tutorial_billing.html)\.

1. Back in the list of groups, select the check box for your new group\. Choose **Refresh** if necessary to see the group in the list\.

1. Choose **Next: Tags**\.

1. \(Optional\) Add metadata to the user by attaching tags as key\-value pairs\. For more information about using tags in IAM, see [Tagging IAM Entities](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_tags.html) in the *IAM User Guide*\.

1. Choose **Next: Review** to see the list of group memberships to be added to the new user\. When you are ready to proceed, choose **Create user**\.

You can use this same process to create more groups and users and to give your users access to your AWS account resources\. To learn about using policies that restrict user permissions to specific AWS resources, see [Access Management](https://docs.aws.amazon.com/IAM/latest/UserGuide/access.html) and [Example Policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_examples.html)\.

## Sign in as an IAM user<a name="signing-in-iam-user-gsg"></a>

After you create an IAM user, you can sign in to AWS with your IAM user name and password\.

Before you sign in as an IAM user, you can verify the sign\-in link for IAM users in the IAM console\. On the IAM Dashboard, under **IAM users sign\-in link**, you can see the sign\-in link for your AWS account\. The URL for your sign\-in link contains your AWS account ID without dashes \(‐\)\. 

If you don't want the URL for your sign\-in link to contain your AWS account ID, you can create an account alias\. For more information, see [Creating, Deleting, and Listing and AWS Account Alias](https://docs.aws.amazon.com/IAM/latest/UserGuide/console_account-alias.html#CreateAccountAlias) in the *IAM User Guide*\.

**To sign in as an AWS user**

1. Sign out of the AWS Management Console\.

1. Enter your sign\-in link\.

   Your sign\-in link includes your AWS account ID \(without dashes\) or your AWS account alias:

   ```
   https://aws_account_id_or_alias.signin.aws.amazon.com/console
   ```

1. Enter the IAM user name and password that you just created\. 

   When you're signed in, the navigation bar displays "*your\_user\_name* @ *your\_aws\_account\_id*"\. 
