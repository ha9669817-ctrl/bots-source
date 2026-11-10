# bots-source

هذا المستودع مُعدّ لرفع الملفات الكبيرة باستخدام **Git LFS**. لا ترفع ملفًا بحجم 390 MB عبر Git العادي؛ GitHub يرفض الملفات العادية التي تتجاوز 100 MiB.

## رفع ملفك (حوالي 390 MB)

1. ثبّت [Git LFS](https://git-lfs.com/) ثم نفّذ مرة واحدة:

   ```bash
   git lfs install
   ```

2. استنسخ المستودع:

   ```bash
   git clone https://github.com/ha9669817-ctrl/bots-source.git
   cd bots-source
   ```

3. ضع الملف المضغوط داخل مجلد المستودع. الأنواع الشائعة (`.zip`, `.7z`, `.rar`, `.gz`, `.tar`) مُعدّة للتتبع عبر Git LFS في `.gitattributes`.

4. أضف الملف وادفعه:

   ```bash
   git add .
   git commit -m "Add large archive"
   git push
   ```

إذا كان امتداد الملف غير موجود في `.gitattributes`، أضف تتبعه قبل `git add`، مثلًا: `git lfs track "*.امتداد"`، ثم أضف ملف `.gitattributes` وادفع التغييرات.

## ملاحظة عن الأحجام

الملف المضغوط بحجم 390 MB أقل من حد Git LFS البالغ 2 GB للملف الواحد على خطتي GitHub Free وPro. أما الملف الأصلي بحجم يقارب 1 GB، فلا ترفعه أيضًا إلا إذا كان تتبعه عبر Git LFS. قد تُطبّق حصص أو تكاليف تخزين ونقل بيانات Git LFS على الحساب؛ راجع [توثيق Git LFS والفوترة](https://docs.github.com/en/billing/concepts/product-billing/git-lfs).
