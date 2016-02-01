CKEditor Package
=====================

## Installation
### Set up package

```
composer require midium/laravel-ckeditor:dev-master
```

### Add ServiceProvider

Edit config/app.php, add the following file to `Application Service Providers` section.
```
Midium\Ckeditor\ServiceProvider::class,
```

### Publish the package's config and assets
```
php artisan vendor:publish --tag=ckedit
```

## Usage

Default way (initiate by name or id) :

```javascript
    <script src="/vendor/midium/laravel-ckeditor/ckeditor.js"></script>
    <script>
        CKEDITOR.replace( 'article-ckeditor' );
    </script>
```

Or if you want to initiate by jQuery selector :

```javascript
    <script src="/vendor/midium/laravel-ckeditor/adapters/jquery.js"></script>
    <script src="/vendor/midium/laravel-ckeditor/ckeditor.js"></script>
    <script>
        $('textarea').ckeditor();
        // $('.textarea').ckeditor(); // if class is prefered.
    </script>
```

## File Uplader Integration

 Instead of using KCFinder, we recommend [laravel-filemanager](https://github.com/UniSharp/laravel-filemanager) for the file uploader integration for better laravel user access control and specific per user folders.
