Heavy-handed-social-ticker
==========================

My take on Scotch.io's social ticker, which takes forever to terminate if an article is popular: compress it to 3 seconds.

![scotch.io social ticker](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAPQAAACaCAMAAACpD5XmAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyFpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuNS1jMDIxIDc5LjE1NDkxMSwgMjAxMy8xMC8yOS0xMTo0NzoxNiAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENDIE1hY2ludG9zaCIgeG1wTU06SW5zdGFuY2VJRD0ieG1wLmlpZDo3NTREODI2REUzQUUxMUUzOTdGRDgzMTc5MzI3MTdEMSIgeG1wTU06RG9jdW1lbnRJRD0ieG1wLmRpZDo3NTREODI2RUUzQUUxMUUzOTdGRDgzMTc5MzI3MTdEMSI+IDx4bXBNTTpEZXJpdmVkRnJvbSBzdFJlZjppbnN0YW5jZUlEPSJ4bXAuaWlkOjc1NEQ4MjZCRTNBRTExRTM5N0ZEODMxNzkzMjcxN0QxIiBzdFJlZjpkb2N1bWVudElEPSJ4bXAuZGlkOjc1NEQ4MjZDRTNBRTExRTM5N0ZEODMxNzkzMjcxN0QxIi8+IDwvcmRmOkRlc2NyaXB0aW9uPiA8L3JkZjpSREY+IDwveDp4bXBtZXRhPiA8P3hwYWNrZXQgZW5kPSJyIj8+YsDQdgAAABhQTFRF////3Nzc0EM5n9XjQ22kv4Fwe5m94rmgWd3/IwAABYBJREFUeNrsnIuWoyAMhhsh5P3feLlrvWCQ2HbW/OdsdTtjmo8kIOD09VKpVCqVSqVSqVQqlUpe0KW/ZknCfusTftGSjP3jT/hFSwqt0Aqt0Ar9v0Kj9XLpnKzNb3iZXlflLMVLkx3M19cTCWhc+hVP7EVX5SwlW7nt0vW0MTQG7fJL+ijz3tJd0FKWUvvVtns7kavp5CrZpavuUiWKWPKXp6ai0mD03nJy0N4wFVfXH/JhS5Qv89bIueWJHHTyMPhbXF2FBz5uqUDnUkYrWtPpA1yuvWyX1hX0DUsJ2oVuez6Rgk6ehlciW/ohd2V0lbM0p3fsxEw9EYLO7lEZX9xOeODDlu6GLiEB5xWyyGxGGX6fK2Rpmd6p4eqJ6M1JHQ7NXnjgs5bmTr+mTD25C3obHvispRk63ny65YlOOBRaoRVaoRX6f4d+5LbOMzfwVCqVSqVSqVQ/JzDGOWetfzFm7BYPvK2kwXtFIELEafIvRCBP7Oyb3GXuClzBLxN73KVQlBtWxGWxVQL5KjasiDM33Ip8CXsX+Qr2PrIctrENGRHkbmyaGqKbmbuom8xd1E1mAWpnT+SEmDuocToR3szMpjYMCTEPUjOYmdTAgQYh5iFqY1kyQswsappYopuZGdRMZgY1k/kyNVi2JAqaVdYwsXVjQbPKGvjQIFDQA2V9FGgXpx0rgVCgT0LdEehpAqlA5xtP1xVq6IEGoUBfCjW0ircv1MYIhXobaD+hTM91hMjCcKhNq3ZdTwcOfdDA77rx5SfSNQE20CST3RHN7NR0K7/bQfVNAtxQr+fPsRWwZMAGGmWyO0ahd9Rak27ouNCwGZRKQHGKIY+rKAOjljmEhs4bFNhkL6zhmPlNm0CWI+FuMtAPQee3jlKBC00Zego/2Y00CZR086eOW9K1JQ47OnZJ53fycVPT3UXdhrYD0HDau3NH6VLlOeLj0PYuaDjv3Y8s7cwpKB4wj9l3QGd3vFs93fcp0mXoOFoRNe7TBKCbHZm9nN7XoZej9Feg2TW9poYh6KkFLdGR3QPNv/vGg8UC+APQ5uzOnA+NeSfnW9Dcm5NVqKFjxoGbzQwI+3dwGOufuSNbcfVMszZ3ZDTNN98S0NAL3THLgvaskznhoPn/cLBeKDO1PIZmTy3hdNLJnFouSHEfun/pxPRBdywipI14gMFFhEXk8bBjl8hvaM+0P7pctKhkIKmVwb38Dn9aZLrXgMWg3wNaQ08gtgbcsdb/pSXgmL5wuEF/aXf+Dyz243rZYHgP75HbOo/cwHvmVu0zN+Wf+fjFMx+0eeYjVc98eK6V4q7Xkthjki+8LbWrr3IPxI70YO8+3ftAbArR4x59Ls7OD7kPmrrlIfeXSqVSqVQqlUqlUql+UhQnzmQHJ5Mk/cU6lM0Ne7YzX82rQjhomjhLamh6DbrXsGd7flgH5J3B8UhHU83f6Vlyo2AtNOIt0BUeU5wwNTCF7941scEd102TX6Kf6OrFVGLWsdJIyYmUg9U04JXVyi102nkOxhK1N5ryPSRr+MJXZH5KRPXlEv4FYFcuzsdQSXgNGktTIt+dVk1j2nDHsBtbMil9VnrbzNnAgQ6/HAIb/lcuLkfqS+/4Nc9mDS2T62Rr5eQsyj2bywlw+hjCCtrDYnC4fFtsPfZCp35xBW2FsLH03pTMGqrdOcY/x+tI7xBO9JnsYoTTxeVIvR0ZFLOLkKBATcNrrpxoNqT5Etp0tF383Zw4i2FwWTWvrpp+g85mwFqBKONbeqc3XI2bjxL2RDp1BtFmubgcQwfnLkGnrjB45wxKQJcRKkPH4SV6amppGf6QFa/IL/ViquXJd7hCU7nS5Zq2+n2KKpVKpVKpVCqVSqVSqVQqlUqleqL+CTAA3FVoYXfSkvkAAAAASUVORK5CYII=)
