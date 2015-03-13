

link_with 'AssetsSample3', 'UnitTests'
pod '1PasswordExtensionHaha'

target 'AssetsSample1' do
  # Not :exclusive on purpose so we can ensure we don't try to integrate the resources twice for this target
  # (one because in inherit the root and one because it redeclare it specifically)
  pod '1PasswordExtensionHaha'
end

target 'AssetsSample2', :exclusive => true do
  pod 'OHHTTPStubs'
end

# Resources of 1PasswordExtensionAhah should be added for AssetsSample1, AssetsSample3 and UnitTests
# but not for AssetsSample2
