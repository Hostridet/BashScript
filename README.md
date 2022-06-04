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
