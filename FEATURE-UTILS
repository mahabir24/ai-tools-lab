"""Small general-purpose utility functions."""


def is_palindrome(s: str) -> bool:
    """Check whether a string is a palindrome.

    The comparison ignores case, spaces, and punctuation, so phrases like
    "A man, a plan, a canal: Panama" are treated as palindromes.

    Args:
        s: The string to check.

    Returns:
        True if the cleaned string reads the same forwards and backwards,
        False otherwise. An empty string (or one with no letters/digits)
        counts as a palindrome.

    Examples:
        >>> is_palindrome("Racecar")
        True
        >>> is_palindrome("hello")
        False
    """
    cleaned = "".join(ch.lower() for ch in s if ch.isalnum())
    return cleaned == cleaned[::-1]


def count_words(text: str) -> int:
    """Count the number of words in a piece of text.

    Words are sequences of non-whitespace characters separated by any
    amount of whitespace (spaces, tabs, or newlines).

    Args:
        text: The text to analyse.

    Returns:
        The number of words in the text. Returns 0 for an empty string or
        a string containing only whitespace.

    Examples:
        >>> count_words("The quick  brown fox")
        4
        >>> count_words("   ")
        0
    """
    return len(text.split())


def celsius_to_fahrenheit(c: float) -> float:
    """Convert a temperature from degrees Celsius to degrees Fahrenheit.

    Uses the formula F = C * 9/5 + 32.

    Args:
        c: Temperature in degrees Celsius.

    Returns:
        The equivalent temperature in degrees Fahrenheit.

    Examples:
        >>> celsius_to_fahrenheit(0)
        32.0
        >>> celsius_to_fahrenheit(100)
        212.0
    """
    return c * 9 / 5 + 32


if __name__ == "__main__":
    import doctest

    doctest.testmod()
