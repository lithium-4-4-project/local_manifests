Manifests for kernel 4.4 project
=========================================

Copy to .repo/local_manifests directory in your ROM source

Some ROMs dont allow for overriding the QCOM HALs or they don't override the HALs properly.

The most obvious symptom is no graphics when trying to boot a fresh build.

The fix for this is very easy. Navigate to the hardware/qcom-caf directory of your ROM source.

Delete the msm8996 directory, then rename the msm8996-r directory to msm8996.

Remove this line from msm8996-common/msm8996.mk: QCOM_SOONG_NAMESPACE := hardware/qcom-caf/msm8996-r

That's it :)
