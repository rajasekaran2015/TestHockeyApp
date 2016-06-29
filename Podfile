# Uncomment this line to define a global platform for your project
platform :ios, '8.0'
workspace 'TestHockeyApp'

target 'TestHockeyApp' do
  # Comment this line if you're not using Swift and don't want to use dynamic frameworks
  use_frameworks!

  # Pods for TestHockeyApp
    pod 'HockeySDK'
  target 'TestHockeyAppTests' do
    inherit! :search_paths
    # Pods for testing
  end

  target 'TestHockeyAppUITests' do
    inherit! :search_paths
    # Pods for testing
  end

end

post_install do |installer|
    installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            config.build_settings['EXPANDED_CODE_SIGN_IDENTITY'] = ""
            config.build_settings['CODE_SIGNING_REQUIRED'] = "NO"
            config.build_settings['CODE_SIGNING_ALLOWED'] = "NO"
        end
    end
end