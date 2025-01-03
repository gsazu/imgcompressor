# Image Compressor.

This is a android library that compress the image size to the minimum for visible.

## How to implement ?

To implement it in your project you can add the below dependency in your `app/buid.gradle`

```gradle
dependencies {
    ...
	implementation 'io.github.gsazu:imgcompressor:0.0.3'
}
```


## How to call ?

To call the image Compressor, you can use the below example code:

```koltin
DsCompressor(context, lifecycleScope).compressImage(uri,object: OnImageCompressListener {
                override fun onImageCompress(result: DsCompressorResult) {
                    if(result.imageBitmap != null){
                        binding.ivView.setImageBitmap(result.imageBitmap)
                    }

                    if(result.imageUri != null){
                        binding.tvResult.text = result.imageUri.toString()
                    }
                }
            })
```

`DsCompressorResult` rerturns imageBitmap, imageUri and byteArray that you can use it in your own way.
Thank you.
