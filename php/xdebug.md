# Installing Xdebug for PHP

1. **Download the TS version** according to your PHP version from [Xdebug Downloads](https://xdebug.org/download).

    You will get a file like `php_xdebug-x.x.x-X.X-TS-vsXX-x86_64.dll`.

2. **Rename the file** to `php_xdebug.dll` and place it in your `php/ext` folder.

    For example, in XAMPP, it is located at `C:\xampp\php\ext`.

3. **Add the following lines** to your `php.ini` file:

    ```ini
    [XDebug]
    xdebug.mode=debug
    xdebug.start_with_request=yes
    xdebug.client_port=9003
    xdebug.client_host=localhost
    zend_extension="C:\xampp\php\ext\php_xdebug.dll"
    ```

4. **Optional**: If you encounter the following warning when running any PHP file:

    ```
    Xdebug: [Step Debug] Time-out connecting to debugging client, waited: 200 ms. Tried: localhost:9003 (through xdebug.client_host/xdebug.client_port).
    ```

    Change `xdebug.start_with_request=yes` to `xdebug.start_with_request=trigger` in your `php.ini` file.
