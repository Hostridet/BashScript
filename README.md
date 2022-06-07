Приветствуем пользователя по имени, создаем файл, если такого не существует. Если такой файл уже существует, то он выводится в случае, если был создан ранее, чем 5 дней назад.
```
#!/bin/bash

echo "Hello, $name, how are you?"
if [[ ! -f $file_name ]]
	then
		touch $file_name
		echo "$name, file $file_name was created"
	else
		echo "$name, file $file_name already consists, if it was created more than 5 days ago he will not be written:"
		find $file_name  -mtime -5
fi
```
![image](https://user-images.githubusercontent.com/71911447/172342941-51ceadd2-415c-4765-becf-8b49f44bf3e5.png)
![image](https://user-images.githubusercontent.com/71911447/172342952-f4f9e27e-cace-4fb4-a66f-17a507dcb5d5.png)

