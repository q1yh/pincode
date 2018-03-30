# Android APP Pincode
Example of add pincode protection to Android APP when launching or resume.

Call pincode interface:
The pincode interface could be called under onCreate() or onResume() function of the calling activity.
'''
startActivity(new Intent(this, PinCodeActivity.class));
'''

Pincode session timeout:
The last successfully pincode verification time is recorded under key "lastPassVeriTime" of SharedPreference.
'''
SharedPreferences.getLong("lastPassVeriTime",0);
'''
By comparing the now and last verified time, the pincode session timeout could be archieved easily.
