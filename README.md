# test_new_plugin
測試cordova-plugin-cosmos-beacon用

## Project setup
```bash
$ npm install
$ cordova plugin add --link ../cordova-plugin-cosmos-beacon
```

### Build android
(若platforms下還沒有android的專案時)
```bash
$ npm run build
$ cordova platform add android
```

### Rebuild android
```bash
$ ./test_android.sh
```