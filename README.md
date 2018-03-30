# Android APP Pincode
Here is an example of add pincode protection to Android APP when launching or resume, in case where certain privacy protection is need for some APPs and the access of their contents.


- Call pincode interface:

The pincode interface could be called under onCreate() or onResume() function of the calling activity.
```
startActivity(new Intent(this, PinCodeActivity.class));
```


- Pincode session timeout:

The last successfully pincode verification time is recorded under key "lastPassVeriTime" of SharedPreference.
```
SharedPreferences.getLong("lastPassVeriTime",0);
```
By comparing the now and last verified time, the pincode session timeout could be archieved easily.
