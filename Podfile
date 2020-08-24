#AYLA_COCOAHTTPSERVER: default to "https://github.com/AylaNetworks/CocoaHTTPServer_Public"
platform :ios, '10.0'

require_relative './Podhelper'
conditional_assign("ayla_cocoahttpserver", "https://github.com/AylaNetworks/CocoaHTTPServer_Public")

target :iOS_AylaSDK do
    pod 'AFNetworking', '~> 3.0'

    pod 'CocoaHTTPServer',
    :git => @ayla_cocoahttpserver,
    :branch => "master"

    pod 'SocketRocket', '~> 0.4'
    pod 'QNNetDiag'
end

target :iOS_AylaSDKTests do
	pod 'AFNetworking/Reachability', '~> 3.0'
	pod 'AFNetworking/Serialization', '~> 3.0'
	pod 'AFNetworking/Security', '~> 3.0'
	pod 'AFNetworking/NSURLSession', '~> 3.0'

    pod 'CocoaHTTPServer',
    :git => @ayla_cocoahttpserver,
    :branch => "master"

    pod 'SAMKeychain'
    pod 'SocketRocket', '~> 0.4'
    pod 'QNNetDiag'
    pod 'OCMock', '~> 3.2'
    pod 'OHHTTPStubs', '~> 5.0'
end

post_install do |installer|
  installer.pods_project.build_configurations.each do |config|
    config.build_settings['GCC_WARN_INHIBIT_ALL_WARNINGS'] = 'YES'
  end
end
