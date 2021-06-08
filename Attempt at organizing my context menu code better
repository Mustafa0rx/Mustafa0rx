import UIKit

class ViewController: UIViewController {
    var contextMenuDataSource = CommentsContextMenuHandler()
    
    override func viewDidLoad() {
        super.viewDidLoad()
        
        let interaction = UIContextMenuInteraction(delegate: contextMenuDataSource)
        view.addInteraction(interaction)
    }
}

class CommentsContextMenuHandler: NSObject, UIContextMenuInteractionDelegate {
    func contextMenuInteraction(_ interaction: UIContextMenuInteraction, configurationForMenuAtLocation location: CGPoint) -> UIContextMenuConfiguration? {
        return UIContextMenuConfiguration(identifier: nil, previewProvider: createFancyViewController) { (suggestElements) in
            return UIMenu(inlineWithActions: [
                UIAction(action: .upvote, handler: self.upvote(action:)),
                UIAction(action: .downvote, handler: self.downvote(action:))
            ])
        }
    }
    
    // MARK: - View Controller Creation
    
    func createFancyViewController() -> UIViewController {
        // Would likely do more customization here typically
        return UIViewController()
    }
    
    // MARK: - Actions
    
    func upvote(action: UIAction) {
        // Do an upvote!
    }
    
    func downvote(action: UIAction) {
        // Do a downvote!
    }
}

extension UIMenu {
    convenience init(inlineWithActions actions: [UIAction]) {
        self.init(title: "", image: nil, identifier: nil, options: .displayInline, children: actions)
    }
}

enum Action: String {
    case upvote
    case downvote
    
    var title: String {
        switch self {
        case .upvote:
            return "Upvote"
        case .downvote:
            return "Downvote"
        }
    }
    
    var icon: UIImage {
        switch self {
        case .upvote:
            return UIImage(systemName: "arrow.up")!
        case .downvote:
            return UIImage(systemName: "arrow.down")!
        }
    }
}

extension UIAction {
    convenience init(action: Action, handler: @escaping UIActionHandler) {
        self.init(title: action.title, image: action.icon, identifier: UIAction.Identifier(rawValue: action.rawValue), handler: handler)
    }
}import UIKit

class ViewController: UIViewController {
    var contextMenuDataSource = CommentsContextMenuHandler()
    
    override func viewDidLoad() {
        super.viewDidLoad()
        
        let interaction = UIContextMenuInteraction(delegate: contextMenuDataSource)
        view.addInteraction(interaction)
    }
}

class CommentsContextMenuHandler: NSObject, UIContextMenuInteractionDelegate {
    func contextMenuInteraction(_ interaction: UIContextMenuInteraction, configurationForMenuAtLocation location: CGPoint) -> UIContextMenuConfiguration? {
        return UIContextMenuConfiguration(identifier: nil, previewProvider: createFancyViewController) { (suggestElements) in
            return UIMenu(inlineWithActions: [
                UIAction(action: .upvote, handler: self.upvote(action:)),
                UIAction(action: .downvote, handler: self.downvote(action:))
            ])
        }
    }
    
    // MARK: - View Controller Creation
    
    func createFancyViewController() -> UIViewController {
        // Would likely do more customization here typically
        return UIViewController()
    }
    
    // MARK: - Actions
    
    func upvote(action: UIAction) {
        // Do an upvote!
    }
    
    func downvote(action: UIAction) {
        // Do a downvote!
    }
}

extension UIMenu {
    convenience init(inlineWithActions actions: [UIAction]) {
        self.init(title: "", image: nil, identifier: nil, options: .displayInline, children: actions)
    }
}

enum Action: String {
    case upvote
    case downvote
    
    var title: String {
        switch self {
        case .upvote:
            return "Upvote"
        case .downvote:
            return "Downvote"
        }
    }
    
    var icon: UIImage {
        switch self {
        case .upvote:
            return UIImage(systemName: "arrow.up")!
        case .downvote:
            return UIImage(systemName: "arrow.down")!
        }
    }
}

extension UIAction {
    convenience init(action: Action, handler: @escaping UIActionHandler) {
        self.init(title: action.title, image: action.icon, identifier: UIAction.Identifier(rawValue: action.rawValue), handler: handler)
    }
}
