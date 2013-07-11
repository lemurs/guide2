```ObjC
//
//  ClassName.m
//  AppName
//

#import "ClassName.h" // Counterpart always comes first

#import "AlphabeticallyOrdered.h" // Use newline if breaking alphabetical order
#import "OtherClassNames.h"
#import <System/Frameworks.h> // System imports come last


@interface ClassName () // If it can be private, make it private!
+ (id)staticMember;
@end


@iimplementation ClassName

+ (instancetype)className;
{
    // Four spaces per indent. Do not use tabs.
}

- (instancetype)customInitializer;
{
    if (!(self = [super init]))
        return nil; // Always use early returns
        
    // So the code has a leftward biased shaped
    
    return self;
}


#pragma mark - NSObject

- (NSString *)description;
{
    // The idea here is to group methods by which class declares them,
    // starting at NSObject, down the inheritance hierarchy, leading
    // into an alphabetical list of protocols, then finally, API

    // Use hyphens in major sections, but not subsections
    // Two newlines above a pragma
    
    return @"";
}


#pragma mark - UITableViewDataSource


#pragma mark - UITableViewDelegate


#pragma mark - API

+ (void)classMethods;
{
    // In general, order class methods above instance methods
}

+ (id)staticMember;
{
    static const staticMember;
    return staticMember ? : (staticMember = [MemberClass factoriesPrefered]);
}

- (NSString *)string; // Property overrides comes first
{
    // Accessors grouped with mutators
}

- (void)setString:(NSString *)string;
{
    // Accessors before mutators
}

- (IBAction)action; // Actions come next
{

}

- (IBAction)anotherAction; // In alphabetical order, of course
{

}

// Then other methods
- (void)otherMethods:(id)type otherThanActions:(NSUInteger)useWidthAgnosticScalars;
{
    // Note the use of Oxford semicolons at the end of method declarations.
}

@end

NSString * const kOtherConstants = @"Use explicit constants. Avoid inline constants.";
NSString * const kPropertyKey = @"It's good to define constants for every property";
// There should always be a newline at the end of the file!

```
