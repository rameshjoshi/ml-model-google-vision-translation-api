**Scenario** : take a photo that has been uploaded, examine it for text, extract any text that is found, translate that text into various languages, and then store those translations for easy retrieval.

****Steps**** **used in the solutions**:
  1. Enable APIs.
  2. Create Cloud Storage buckets.
  3. Create Cloud Pub/Sub topics.
  4. Create and deploy Cloud Functions.
  5. Upload an image to initiate test.
  6. View the results.

![image](https://github.com/rameshjoshi/ml-model-google-vision-translation-api/assets/7277702/009c7b5e-26d8-4fef-aafd-6a48b7476cb7)

Cloud Resources
  Storage bucket: app1-uploaded-images, app1-translated-images
  Topics: app1-image-to-text, app1-image-to-text-translation
  functions: app1-ocr-extract, app1-ocr-save, app1-ocr-translate

**Vision AI**
Derive insights from images in the cloud or at the edge with AutoML Vision or use pre-trained Vision API models to detect objects, understand text, and more.

**Translation AI**
Make your content and apps multilingual with fast, dynamic machine translation


**Test (mannual)**
1. Copy the sign.png file to uploaded-images bucket
  gsutil cp sign.png gs://app1-uploaded-images
  Navigate to the translated-results bucket, and you will see a list of .txt files for all translations.
2. copy the menu.jpg file to uploaded-images bucket
   gsutil cp menu.jpg gs://app1-uploaded-images
   Verify the menu.jpg image file was uploaded successfully by opening your bucket for uploaded-images
