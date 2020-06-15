# Удаление объектов и бакетов<a name="DeletingAnObjectandBucket"></a>

Когда необходимость в объектах и бакетах пропадает, мы рекомендуем вам их удалить, чтобы избежать последующих расходов\. Если вы выполнили это пошаговое руководство по началу работы в качестве учебного упражнения и не планируете использовать свои объекты или бакеты, мы рекомендуем вам удалить бакет, чтобы не было дополнительных расходов\. Прежде чем вы удалите свой бакет, вы должны опустошить бакет или удалить объекты в бакете\. После того, как вы удалите ваши объекты и бакеты, они станут недоступны\.

Если вы планируете продолжать использовать то же имя бакета, мы рекомендуем вам удалить все объекты или очистить бакет, но не удалять бакет\. После удаления бакета, его имя становится доступно к повторному использованию\. В любом случае, другой клиент может создать бакет с таким же именем, до того, как вы заново его используете\. 

**Темы**
+ [Опустошение вашего бакета](#clean-up-empty-bucket)
+ [Удаление объекта](#clean-up-delete-objects)
+ [Удаление бакета](#clean-up-delete-bucket)

## Опустошение бакета<a name="clean-up-empty-bucket"></a>

Если вы планируете удалить свой бакет, вы сначала должны его опустошить, что удалит все объекты в бакете\. 

**Для опустошения бакета**

1. В списке **Buckets** выберите бакет, который вы хотите опустошить и нажмите **Empty**\.

1. Для подтверждения того, что вы хотите опустошить бакет и удалить все объекты в нем, в окне **Empty bucket** введите имя бакета\.
**Важно**  
Опустошение бакета не может быть отменено\. Объекты, добавленные в бакет во время выполнения опустошения бакета, будут удалены\.

1. To empty the bucket and delete all the objects in it, and choose **Empty**\.

   An **Empty bucket: Status** page opens that you can use to review a summary of failed and successful object deletions\.

1. To return to your bucket list, choose **Exit**\.

## Deleting an object<a name="clean-up-delete-objects"></a>

If you want to choose which objects you delete without emptying all the objects from your bucket, you can delete an object\. 

1. In the **Buckets** list, choose the name of the bucket that you want to delete an object from\.

1. In the **Name** list, select the check box for the object that you want to delete\.

1. Choose **Actions**, and then choose **Delete**\.

1. In the **Delete objects** dialog box, verify that the name of the object, and choose **Delete**\.

## Deleting your bucket<a name="clean-up-delete-bucket"></a>

After you empty your bucket or delete all the objects from your bucket, you can delete your bucket\.

1. To delete a bucket, in the **Buckets** list, select the bucket\.

1. Choose **Delete**\.

1. To confirm deletion, in **Delete bucket**, enter the name of the bucket\.
**Important**  
Deleting a bucket cannot be undone\. Bucket names are unique\. If you delete your bucket, another AWS user can use the name\. If you want to continue to use the same bucket name, don't delete your bucket\. Instead, empty and keep the bucket\. 

1. To delete your bucket, choose **Delete bucket**\.

For more information about using Amazon S3, see [Where do I go from here?](ImplementingS3.md)
