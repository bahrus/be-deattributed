# be-deattributed

## Lingo

```html
<my-tag be-deattributed 
    index-n=5 label=hello 
    with type, icon, in host.options@index;
></my-tag>
```

produces object:

```JavaScript
oMyTag.beDecorated.deattributed.instructions = [
    {
        be: 'set',
        having: {
            props: {
                index: 5,
                label: 'hello'
            }
        }
    },
    {
        be: 'observant',
        having: {
            props: {
                type: 'type',
                icon: {
                    vft: 'options{index}.icon',
                    valPathSubstitutions: ["index"]
                }
            }
        }
    }
];
```