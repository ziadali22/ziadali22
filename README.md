### Hi there 👋, my name is Ziad Ali
#### I am IOS Developer 
[<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/linkedin.svg' alt='linkedin' height='40'>](https://www.linkedin.com/in/https://www.linkedin.com/in/ziad-ali//)  

```swift

import Foundation

struct Profile: CustomStringConvertible {
    
    let name = "Ziad Ali"
    
    var description: String {
        """
        \(name)\n
        I am a software engineer focused on iOS development.
        Working on teams with project managers, developers, 
        and designers, I have built mobile applications and 
        SDKs focused on excellent user experience and design.
        I am looking to work in a collaborative environment 
        where I can develop products that improve people's lives.\n
        """
    }
    
    enum Skill: String, CaseIterable {
        case swift,  uIKit, swiftUI
        case networking, git, alamofire
    }
    
    func proficient(in skills: [Skill] = Skill.allCases) -> String {
        skills
            .map(\.rawValue)
            .map(\.capitalized)
            .map { "- " + $0 + "\n" }
            .reduce("Skills: \n", +)
    }
}

// Paste into a playground!
let profile = Profile()
print(profile.description)
print(profile.proficient())


```


