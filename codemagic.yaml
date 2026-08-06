workflows:
  flet-android-build:
    name: Build Mahmoud ERP APK
    max_build_duration: 15
    instance_type: mac_mini_m1
    environment:
      groups:
        - android-signing
      vars:
        FLET_PRODUCT_NAME: "mahmoud"
      python: 3.10
      java: 17
    scripts:
      - name: Install Flet Tool
        script: |
          pip install flet
      - name: Build Mahmoud ERP APK
        script: |
          flet build apk --product "$FLET_PRODUCT_NAME" --release
    artifacts:
      - build/apk/*.apk
    publishing:
      email:
        recipients:
          - mahmuodnassni@gmail.com # سيتم إرسال الـ APK الجاهز فوراً إلى بريدك هنا
        notify:
          success: true
          failure: true
