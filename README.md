# jodit-vue
Jodit wrapper for Vue JS

###example
```
<template>
    <div>
        <Editor model="description" options="options"/>
    </div>
</template>
<script>

    import 'jodit/build/jodit.min.css'
    import jodit from 'jodit-vuejs'

    export default {
        components: {
            'Editor': jodit
        },
        data: function() {
            return {
                description: '',
                options: {
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
            }
        },
    }
</script>
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