var str = 'date-format-elementui-antd'
function formatHump(str,temp){
    var arr = str.split(temp)
    var newStr = ''
    for(var i = 0;i < arr.length;i++){
        if(i == 0){
            newStr += arr[i]
        }else if(i !== 0){
            arr[i] = arr[i][0].toUpperCase() + arr[i].substr(1)
            newStr += arr[i]
        }
    }
    return newStr
}
formatHump(str,'-')
