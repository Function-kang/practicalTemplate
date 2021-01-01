let arr = [
    {
        name: 'elementUI',
        id: '',
    },
    {
        name: 'elementUI-1',
        id: 'elementUI'
    },
    {
        name: 'elementUI-2',
        id: 'elementUI'
    },
    {
        name: 'elementUI-1-1',
        id: 'elementUI-1'
    },
    {
        name: 'elementUI-1-2',
        id: 'elementUI-1'
    },
    {
        name: 'elementUI-1-3',
        id: 'elementUI-1'
    },
    {
        name: 'elementUI-2-1',
        id: 'elementUI-2'
    },
    {
        name: 'elementUI-2-2',
        id: 'elementUI-2'
    },
    {
        name: 'elementUI-2-3',
        id: 'elementUI-2'
    },
    {
        name: 'elementUI-2-4',
        id: 'elementUI-2'
    },
]

function format(arr){
    let newarr = []
    
    arr.forEach(item=>{
        if(item.id == ''){
            newarr = arr.filter(val=>{
                return val.name == 'elementUI'
            })
        }else{
            arr.forEach(ind => {
            if(item.id == ind.name){
                if(!ind.children){
                    ind.children = []
                }
                ind.children.push(item);
            }
            })
        }
    })

    return newarr
}
format(arr)