Android vnc flinger
-

Come from https://github.com/cyanogen/vncflinger


Put this repo and tigerVnc into external/

You can intergrate it with:

```makefile
# In BoardConfig.mk
BOARD_SEPOLICY_DIRS += external/vncflinger/sepolicy
BOARD_PLAT_PUBLIC_SEPOLICY_DIR += external/vncflinger/sepolicy/public
BOARD_PLAT_PRIVATE_SEPOLICY_DIR += external/vncflinger/sepolicy/private

# In product makefile
PRODUCT_PACKAGES += vncflinger
```

You can use ``adb forward tcp:<FORWARD_PORT> localreserved:vncflinger``
And then visit vnc via ``localhost:<FORWARD_PORT>``

