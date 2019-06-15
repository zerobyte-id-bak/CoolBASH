# CoolBASH
BASH script style

### loader.bash
![Loader](https://raw.githubusercontent.com/zerobyte-id/CoolBASH/master/img/loader-bash.gif)

Sample:
```
function _loader {
    let _progress=(${1}*100/${2}*100)/100
    let _done=(${_progress}*4)/10
    let _left=40-$_done
    _fill=$(printf "%${_done}s")
    _empty=$(printf "%${_left}s")
	printf "\r <[${_fill// /\#}${_empty// /-}]> ${_progress}%%"
}

last=10
for ((i=0;i<=$last;i++))
do
	_loader "$i" "${last}"
	sleep 0.1 
done
```
