# Build instructions

In order to build the ZIP for DevBase run the following:

  UPDATE_BIN="META-INF/com/google/android/update-binary"
  ROMNAME=$(grep -m1 ROMNAME $UPDATE_BIN | cut -d= -f2)
  VERSION=$(grep -m1 VERSION $UPDATE_BIN | cut -d= -f2)
  BASEVERSION=$(grep -m1 BASEVERSION $UPDATE_BIN | cut -d= -f2)

  zip -9 -r $ROMNAME-$VERSION-$BASEVERSION.zip * -x .git/* -x .gitignore
