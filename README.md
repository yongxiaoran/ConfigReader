# configurator
A header only C++ config_reader library that quickly read/write config files.


Examples:

Assume we have a config file called "1.config", the file is:

username:JackBauer //username  
zipcode:94040   
school:foothill   
weight:4.75   

```c++
int main()
{
    ConfigReader::instance()->load("1.config");
    std::cout << ConfigReader::instance()->read<string>("username");
    std::cout << ConfigReader::instance()->read<int>("zipcode");
}
```

use ConfigReader with C++11 auto

```c++
    auto reader = ConfigReader::instance();
    reader->load("1.config");
    reader->read<double>("weight");
```
