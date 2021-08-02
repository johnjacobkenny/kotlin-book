# Running log of concepts

As I pick up different concepts, I will add them here. And I will elaborate on them slowly as time allows.



* var, val
* companion object



suspend function

dot env

Penicillin



#### Kotlin Map Function

```text
// Create a File object for the images directory.
val imageDir = File( "path_to_image_dir" ).listFiles()

// Map the files to Bitmaps.
val bitmaps = imageDir.map { file -> BitmapFactory.decodeFile( file.absolutePath ) }

// Resize them all at once.
val resizedBitmaps = bitmaps.map { image -> Bitmap.createScaledBitmap( image , 128 , 128 , false ) }
```

Kotlin Map Function better example



