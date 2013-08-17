```ObjC
#import "SuperclassName.h" // Or a blank line

@class Avoid, Importing, InHeaders;

@interface ClassName : SuperclassName

+ (instancetype)className; // Factories and initializers up top
+ (void)classMethods; // Treat properties like class methods

- (instancetype)customInitializer;

@property (nonatomic, weak) IBOutlet UIView *view; // Group outlets together
@property (nonatomic) NSArray *array, *differentArray; // Alphabetical list
@property (nonatomic) NSString *string; // Properies grouped by metainfo then type

- (IBAction)action; // Use IBAction for all actions
- (IBAction)anotherAction; // Alphabetical

- (void)otherMethods:(id)type otherThanActions:(NSUInteger)useWidthAgnosticScalars;

@end

extern NSString * const kOtherConstants;
extern NSString * const kPropertyKey;
```
