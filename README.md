# jodit-vue
Jodit wrapper for Vue JS

###how to use
```
<editor v-model="academic.description" :options="{options}"/>
```
### example options 
* more options follow : https://xdsoft.net/jodit/doc/options/
```
{
    width: '100%',
    minHeight: 400,
    uploader: {
        url: 'editor?action=fileUpload'
    },
    filebrowser: {
        ajax: {
            url: 'editor',
        },
    }
}

```